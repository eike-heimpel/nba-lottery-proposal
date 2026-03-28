<script lang="ts">
	import { page } from '$app/state';
	import { goto } from '$app/navigation';
	import { slides } from '$lib/slides';
	import '../app.css';

	let { children } = $props();
	let cooldown = $state(false);
	let touchStartY = $state(0);

	function navigate(direction: 1 | -1) {
		if (cooldown) return;
		const currentIndex = slides.findIndex((s) => s.path === page.url.pathname);
		const nextIndex = currentIndex + direction;
		if (nextIndex >= 0 && nextIndex < slides.length) {
			cooldown = true;
			goto(slides[nextIndex].path);
			setTimeout(() => (cooldown = false), 600);
		}
	}

	function atScrollBoundary(direction: 1 | -1): boolean {
		const el = document.scrollingElement ?? document.documentElement;
		if (direction > 0) {
			return el.scrollTop + el.clientHeight >= el.scrollHeight - 5;
		}
		return el.scrollTop <= 5;
	}

	function handleKeydown(e: KeyboardEvent) {
		if (e.key === 'ArrowRight' || e.key === 'ArrowDown') {
			e.preventDefault();
			navigate(1);
		} else if (e.key === 'ArrowLeft' || e.key === 'ArrowUp') {
			e.preventDefault();
			navigate(-1);
		}
	}

	function handleWheel(e: WheelEvent) {
		if (Math.abs(e.deltaY) < 30) return;
		const direction: 1 | -1 = e.deltaY > 0 ? 1 : -1;
		if (atScrollBoundary(direction)) {
			navigate(direction);
		}
	}

	function handleTouchStart(e: TouchEvent) {
		touchStartY = e.touches[0].clientY;
	}

	function handleTouchEnd(e: TouchEvent) {
		const deltaY = touchStartY - e.changedTouches[0].clientY;
		if (Math.abs(deltaY) < 50) return;
		const direction: 1 | -1 = deltaY > 0 ? 1 : -1;
		if (atScrollBoundary(direction)) {
			navigate(direction);
		}
	}
</script>

<svelte:window
	onkeydown={handleKeydown}
	onwheel={handleWheel}
	ontouchstart={handleTouchStart}
	ontouchend={handleTouchEnd}
/>

<nav class="fixed right-4 top-1/2 z-50 flex -translate-y-1/2 flex-col gap-2.5">
	{#each slides as slide}
		<a
			href={slide.path}
			class="group relative block h-2 w-2 rounded-full transition-all duration-200 {page.url
				.pathname === slide.path
				? 'scale-125 bg-accent'
				: 'bg-text-dim/40 hover:bg-text-dim'}"
			aria-label={slide.label}
		>
			<span
				class="pointer-events-none absolute right-5 top-1/2 -translate-y-1/2 whitespace-nowrap rounded bg-surface-2 px-2 py-1 font-mono text-[11px] text-text-dim opacity-0 transition-opacity group-hover:opacity-100"
			>
				{slide.label}
			</span>
		</a>
	{/each}
</nav>

{@render children()}

<script lang="ts">
	import { page } from '$app/state';
	import { goto } from '$app/navigation';
	import { slides } from '$lib/slides';
	import '../app.css';

	let { children } = $props();

	const currentIndex = $derived(slides.findIndex((s) => s.path === page.url.pathname));
	const hasPrev = $derived(currentIndex > 0);
	const hasNext = $derived(currentIndex < slides.length - 1);

	function navigate(direction: 1 | -1) {
		const nextIndex = currentIndex + direction;
		if (nextIndex >= 0 && nextIndex < slides.length) {
			goto(slides[nextIndex].path);
		}
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
</script>

<svelte:window onkeydown={handleKeydown} />

<nav class="fixed right-20 z-50 hidden -translate-y-1/2 flex-col gap-2.5 md:flex" style="top: 50dvh">
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

<div class="fixed left-0 z-50 -translate-y-1/2 pl-4 md:pl-6" style="top: 50dvh">
	<button
		onclick={() => navigate(-1)}
		disabled={!hasPrev}
		class="flex h-12 w-12 cursor-pointer items-center justify-center rounded-full border border-border/50 bg-surface/50 text-lg text-text-dim backdrop-blur-sm transition-all hover:border-accent hover:text-accent disabled:cursor-default disabled:opacity-0"
		aria-label="Previous slide"
	>
		←
	</button>
</div>

<div class="fixed right-0 z-50 -translate-y-1/2 pr-4 md:pr-6" style="top: 50dvh">
	<button
		onclick={() => navigate(1)}
		disabled={!hasNext}
		class="flex h-12 w-12 cursor-pointer items-center justify-center rounded-full border border-border/50 bg-surface/50 text-lg text-text-dim backdrop-blur-sm transition-all hover:border-accent hover:text-accent disabled:cursor-default disabled:opacity-0"
		aria-label="Next slide"
	>
		→
	</button>
</div>

<div class="fixed bottom-3 left-1/2 z-50 -translate-x-1/2 md:hidden">
	<span class="font-mono text-[11px] text-text-dim/60">
		{currentIndex + 1} / {slides.length}
	</span>
</div>

{@render children()}

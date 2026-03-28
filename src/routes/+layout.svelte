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

<div class="flex h-dvh w-full">
	<!-- Left nav button -->
	<div class="flex w-14 shrink-0 items-center justify-center md:w-16">
		{#if hasPrev}
			<button
				onclick={() => navigate(-1)}
				class="flex h-10 w-10 cursor-pointer items-center justify-center rounded-full border border-border bg-surface text-base text-text-dim transition-all hover:border-accent hover:text-accent"
				aria-label="Previous slide"
			>
				←
			</button>
		{/if}
	</div>

	<!-- Slide content -->
	<main class="flex-1 overflow-y-auto">
		{@render children()}
	</main>

	<!-- Right nav button + dots -->
	<div class="flex w-14 shrink-0 flex-col items-center justify-center gap-6 md:w-16">
		<!-- Nav dots (desktop only) -->
		<nav class="hidden flex-col gap-2.5 md:flex">
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

		{#if hasNext}
			<button
				onclick={() => navigate(1)}
				class="flex h-10 w-10 cursor-pointer items-center justify-center rounded-full border border-border bg-surface text-base text-text-dim transition-all hover:border-accent hover:text-accent"
				aria-label="Next slide"
			>
				→
			</button>
		{/if}

		<!-- Slide counter (mobile only) -->
		<span class="font-mono text-[10px] text-text-dim/50 md:hidden">
			{currentIndex + 1}/{slides.length}
		</span>
	</div>
</div>

<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';
</script>

<SlideLayout
	slideNumber="00"
	background="linear-gradient(165deg, #0a0a0f 0%, #161622 50%, #0d0d15 100%)"
>
	<div
		class="pointer-events-none absolute right-[-200px] top-[-200px] h-[700px] w-[700px] rounded-full"
		style="background: radial-gradient(circle, var(--color-accent-glow) 0%, transparent 70%)"
	></div>

	<div class="relative z-10 max-w-3xl text-center">
		<h1 class="section-title mb-6" style="font-size: clamp(48px, 7vw, 96px)">
			STOP <span class="text-accent">REWARDING</span> FAILURE
		</h1>

		<p class="mx-auto max-w-2xl font-body text-lg leading-relaxed text-text-dim md:text-xl">
			A structural proposal for the NBA: flipped lottery incentives and a King of the Hill draft
			tournament.
		</p>

		<div class="mt-10 border-t border-border pt-4">
			<p class="font-mono text-xs tracking-widest text-text-dim">
				NBA REFORM PROPOSAL — 2025-26 SEASON & BEYOND
			</p>
		</div>
	</div>

</SlideLayout>

<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';
</script>

<SlideLayout slideNumber="—">
	<div class="w-full max-w-4xl">
		<p class="mb-3 font-mono text-[11px] tracking-widest text-text-dim uppercase">Appendix</p>
		<h2 class="section-title mb-10 opacity-70">ADDITIONAL NOTES</h2>

		<div class="space-y-8">
			<div class="border-l-2 border-warm/30 pl-6">
				<h3 class="mb-2 font-heading text-lg font-600 text-text-bright uppercase">
					Scales to 32 teams
				</h3>
				<p class="text-sm leading-relaxed text-text-dim">
					When Seattle and Las Vegas join, the structure scales naturally. More lottery teams means
					a longer King of the Hill chain — 7 games instead of 4. The play-in bracket expands to
					accommodate extra teams. The incentive logic is identical at any league size: winning is
					always rational at every position.
				</p>
			</div>

			<div class="border-l-2 border-warm/30 pl-6">
				<h3 class="mb-2 font-heading text-lg font-600 text-text-bright uppercase">
					Fewer games, better product
				</h3>
				<p class="text-sm leading-relaxed text-text-dim">
					This structure makes it easier to reduce the regular season. When every game matters for
					tier placement and the postseason adds high-stakes single-elimination tournament games,
					the total product improves with fewer regular season games. Less load management, less
					coasting, more intensity — and the KotH and play-in replace lost inventory with premium
					content that draws bigger audiences.
				</p>
			</div>
		</div>
	</div>
</SlideLayout>

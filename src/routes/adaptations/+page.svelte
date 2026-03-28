<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';
</script>

<SlideLayout slideNumber="—">
	<div class="w-full max-w-4xl">
		<p class="mb-3 font-mono text-[11px] tracking-widest text-text-dim uppercase">Appendix</p>
		<h2 class="section-title mb-10 opacity-70">POSSIBLE ADAPTATIONS</h2>

		<div class="space-y-8">
			<div class="border-l-2 border-warm/30 pl-6">
				<h3 class="mb-2 font-heading text-lg font-600 text-text-bright uppercase">
					Sliding play-in consolation
				</h3>
				<p class="text-sm leading-relaxed text-text-dim">
					Instead of flat odds for all play-in losers, scale consolation by elimination order. The
					first team eliminated gets slightly better odds than the second. This narrows the gap
					between the last play-in team and the top KotH seed without changing any structure.
				</p>
			</div>

			<div class="border-l-2 border-warm/30 pl-6">
				<h3 class="mb-2 font-heading text-lg font-600 text-text-bright uppercase">
					8v9 play-in with 7 guaranteed spots
				</h3>
				<p class="text-sm leading-relaxed text-text-dim">
					Shrink the play-in to a single game between the 8th and 9th seeds for the last playoff
					spot. The loser receives flat consolation odds. KotH expands to six teams (10th–15th).
					The boundary team now has a roughly 50/50 shot at the playoffs — making the cost of
					tanking out of that position significantly higher than tanking out of a four-team bracket.
				</p>
			</div>
		</div>
	</div>
</SlideLayout>

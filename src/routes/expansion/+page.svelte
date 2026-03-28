<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';
	import TierBar from '$lib/components/TierBar.svelte';
</script>

<SlideLayout slideNumber="10">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">FUTURE-PROOF</p>
		<h2 class="section-title mb-6">BUILT FOR 32 TEAMS</h2>

		<p class="mb-8 max-w-3xl text-base leading-relaxed text-text-dim">
			When Seattle and Las Vegas join in 2028-29, the system scales naturally. More teams in each
			tier means a longer, more dramatic King of the Hill and an expanded play-in bracket.
		</p>

		<div class="mb-8 overflow-hidden rounded-lg border border-border">
			<TierBar
				rank="1ST — 12TH"
				title="Playoffs (Direct)"
				description="Top 6 per conference. No lottery involvement."
				tier="primary"
			/>
			<TierBar
				rank="13TH — 24TH"
				title="Expanded Play-In (12 Teams → 4 Spots)"
				description="Bottom 8 seeds play down in Round 1. Top 4 seeds (13th–16th) get first-round byes and a safety net — they can lose once. Two parallel brackets, each mirroring the current NBA play-in format. 8 eliminated teams get flat 4.5% lottery odds."
				tier="secondary"
			/>
			<TierBar
				rank="25TH — 32ND"
				title="King of the Hill — 7-Game Chain"
				description="8 teams. 7 single-elimination games. The worst seed starts on the hill. Each round, the next-best seed challenges. A true gauntlet — the 32nd seed must win 7 straight for peak odds. The 25th seed needs just 1 win."
				tier="accent"
			/>
		</div>

		<div class="rounded-lg border border-border bg-surface p-5">
			<p class="text-sm leading-relaxed text-text-dim">
				<span class="font-semibold text-text-bright">Key difference:</span> The 32-team version has a
				longer KotH chain (7 games vs 4) and an expanded play-in bracket. The incentive structure is
				identical — winning is always rational at every position.
			</p>
		</div>
	</div>
</SlideLayout>

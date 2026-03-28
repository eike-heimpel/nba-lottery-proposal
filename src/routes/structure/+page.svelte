<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';
	import TierBar from '$lib/components/TierBar.svelte';
</script>

<SlideLayout slideNumber="04">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">LEAGUE STRUCTURE — 30 TEAMS</p>
		<h2 class="section-title mb-10">THREE TIERS</h2>

		<div class="overflow-hidden rounded-lg border border-border">
			<TierBar
				rank="1ST — 6TH"
				title="Playoffs (Direct)"
				description="Top 6 per conference. 12 teams total. Competing for a championship. No lottery involvement."
				tier="primary"
			/>
			<TierBar
				rank="7TH — 10TH"
				title="Play-In Tournament"
				description="Current NBA format. 4 teams per conference fight for the last 2 playoff spots. The 4 eliminated teams receive flat, equal lottery odds of 4.5% each. No draft incentive to tank within this group."
				tier="secondary"
			/>
			<TierBar
				rank="11TH — 15TH"
				title="King of the Hill — Lottery Tournament"
				description="5 teams per conference play a King of the Hill chain to determine their lottery odds. The higher you finished in the regular season, the later you enter — and the fewer games you need to win. Both conferences run simultaneously."
				tier="accent"
			/>
		</div>
	</div>
</SlideLayout>

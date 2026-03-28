<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';
	import OddsRow from '$lib/components/OddsRow.svelte';
</script>

<SlideLayout slideNumber="03">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">DRAFT LOTTERY ODDS</p>
		<h2 class="section-title mb-10">THE NUMBERS</h2>

		<div class="space-y-1.5">
			<OddsRow label="Play-in eliminated (×4)" pct="4.5%" barWidth={39} emphasis="low" />
			<OddsRow label="KotH — 1st, King (×2)" pct="11.5%" barWidth={100} emphasis="high" />
			<OddsRow label="KotH — 2nd, Final loser (×2)" pct="10%" barWidth={87} emphasis="mid" />
			<OddsRow label="KotH — 3rd (×2)" pct="8.5%" barWidth={74} emphasis="mid" />
			<OddsRow label="KotH — 4th (×2)" pct="6.5%" barWidth={57} emphasis="low" />
			<OddsRow label="KotH — 5th, First eliminated (×2)" pct="4.5%" barWidth={39} emphasis="low" />
		</div>

		<div class="mt-3 text-right font-mono text-xs text-text-dim">
			(4×4.5) + (2×11.5) + (2×10) + (2×8.5) + (2×6.5) + (2×4.5) = 100% ✓
		</div>

		<div class="mt-8 rounded-lg border border-border bg-surface p-5">
			<p class="text-sm leading-relaxed text-text-dim">
				<span class="font-semibold text-text-bright">The bottom line:</span> The team eliminated first
				in the tournament has identical odds (4.5%) to a play-in loser. Being the worst team in your
				conference and losing immediately gets you absolutely nothing extra. Tournament placement determines
				your odds tier.
			</p>
		</div>
	</div>
</SlideLayout>

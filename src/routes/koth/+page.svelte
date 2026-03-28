<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';
	import Matchup from '$lib/components/Matchup.svelte';
</script>

<SlideLayout slideNumber="05">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">THE LOTTERY TOURNAMENT</p>
		<h2 class="section-title mb-6">KING OF THE HILL</h2>

		<p class="mb-8 max-w-3xl text-base leading-relaxed text-text-dim">
			Per conference. 5 teams. 4 games. The worst seed starts on the hill. Each round, the
			next-best seed challenges. Loser is locked into their odds tier. Winner stays on the hill.
		</p>

		<div class="mb-4 font-mono text-xs tracking-wider text-text-dim">
			PER CONFERENCE · ×2 CONFERENCES
		</div>

		<div class="mb-8 flex flex-col items-center gap-0">
			<div class="w-full max-w-sm">
				<div class="mb-1 text-center font-mono text-xs text-text-dim">GAME 1</div>
				<Matchup team1="15th seed" team2="14th seed" />
				<div class="flex justify-end pr-8">
					<span class="mt-1 text-xs text-text-dim">Loser → worst KotH odds</span>
				</div>
			</div>
			<div class="h-2.5 w-0.5 bg-border"></div>

			<div class="w-full max-w-sm">
				<div class="mb-1 text-center font-mono text-xs text-text-dim">GAME 2</div>
				<Matchup team1="Winner" team2="13th seed" />
				<div class="flex justify-end pr-8">
					<span class="mt-1 text-xs text-text-dim">Loser → 4th-best KotH odds</span>
				</div>
			</div>
			<div class="h-2.5 w-0.5 bg-border"></div>

			<div class="w-full max-w-sm">
				<div class="mb-1 text-center font-mono text-xs text-text-dim">GAME 3</div>
				<Matchup team1="Winner" team2="12th seed" />
				<div class="flex justify-end pr-8">
					<span class="mt-1 text-xs text-text-dim">Loser → 3rd-best KotH odds</span>
				</div>
			</div>
			<div class="h-2.5 w-0.5 bg-border"></div>

			<div class="w-full max-w-sm">
				<div class="mb-1 text-center font-mono text-xs text-text-dim">GAME 4</div>
				<Matchup team1="Winner" team2="11th seed" />
				<div class="mt-1 flex justify-between px-4">
					<span class="text-xs text-accent">Winner → best KotH odds</span>
					<span class="text-xs text-text-dim">Loser → 2nd-best KotH odds</span>
				</div>
			</div>
		</div>

		<div class="rounded-lg border border-border bg-surface p-5">
			<h3 class="mb-3 font-heading text-sm font-600 tracking-wider text-text-bright uppercase">
				WHY IT WORKS
			</h3>
			<div class="space-y-2 text-sm text-text-dim">
				<div class="flex items-center gap-3">
					<span class="font-heading text-accent">15th:</span>
					<span>Must win 4 straight for peak odds</span>
					<span class="ml-auto rounded bg-text-bright/5 px-2 py-0.5 font-mono text-xs text-text-dim">Hard</span>
				</div>
				<div class="flex items-center gap-3">
					<span class="font-heading text-accent">13th:</span>
					<span>Must win 2 straight for peak odds</span>
					<span class="ml-auto rounded bg-text-bright/5 px-2 py-0.5 font-mono text-xs text-warm">Tough</span>
				</div>
				<div class="flex items-center gap-3">
					<span class="font-heading text-accent">11th:</span>
					<span>Must win 1 game for peak odds</span>
					<span class="ml-auto rounded bg-text-bright/5 px-2 py-0.5 font-mono text-xs text-text-bright">Fair</span>
				</div>
			</div>
		</div>
	</div>
</SlideLayout>

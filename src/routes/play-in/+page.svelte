<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';
</script>

<SlideLayout slideNumber="05">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">THE PLAY-IN</p>
		<h2 class="section-title mb-6">CURRENT FORMAT, SAME STAKES</h2>

		<p class="mb-8 max-w-3xl text-base leading-relaxed text-text-dim">
			The play-in already works. 7th and 8th seeds get a safety net — they can lose once and still
			advance. 9th and 10th are win-or-go-home.
		</p>

		<div class="mb-4 font-mono text-xs tracking-wider text-text-dim">
			3 GAMES PER CONFERENCE · ×2 CONFERENCES
		</div>

		<div class="mb-8 space-y-4">
			<div class="rounded-lg border border-border bg-surface p-5">
				<div class="mb-1 font-mono text-xs text-text-dim">GAME 1</div>
				<div class="flex items-center gap-3">
					<span class="font-heading text-base text-accent">7th</span>
					<span class="font-mono text-xs text-text-dim">vs</span>
					<span class="font-heading text-base text-warm">8th</span>
					<span class="mx-2 text-text-dim">→</span>
					<span class="text-sm text-text">Winner → <span class="font-semibold text-text-bright">7th seed (playoffs)</span></span>
				</div>
			</div>

			<div class="rounded-lg border border-border bg-surface p-5">
				<div class="mb-1 font-mono text-xs text-text-dim">GAME 2</div>
				<div class="flex items-center gap-3">
					<span class="font-heading text-base text-accent">9th</span>
					<span class="font-mono text-xs text-text-dim">vs</span>
					<span class="font-heading text-base text-warm">10th</span>
					<span class="mx-2 text-text-dim">→</span>
					<span class="text-sm text-text">Loser → <span class="font-semibold text-text-dim">eliminated</span> (4.5% lottery odds)</span>
				</div>
			</div>

			<div class="rounded-lg border border-border bg-surface p-5">
				<div class="mb-1 font-mono text-xs text-text-dim">GAME 3</div>
				<div class="flex items-center gap-3">
					<span class="font-heading text-base text-accent">Loser(G1)</span>
					<span class="font-mono text-xs text-text-dim">vs</span>
					<span class="font-heading text-base text-warm">Winner(G2)</span>
					<span class="mx-2 text-text-dim">→</span>
					<span class="text-sm text-text">Winner → <span class="font-semibold text-text-bright">8th seed</span>, Loser → <span class="font-semibold text-text-dim">eliminated</span> (4.5%)</span>
				</div>
			</div>
		</div>

		<div class="rounded-lg border border-warm/20 bg-surface p-5">
			<h3 class="mb-2 font-heading text-sm font-600 tracking-wider text-warm uppercase">
				THE CONSOLATION
			</h3>
			<p class="text-sm leading-relaxed text-text-dim">
				All 4 eliminated play-in teams (2 per conference) receive identical 4.5% lottery odds. There
				is zero draft incentive to lose within this group. Just compete for the postseason.
			</p>
		</div>
	</div>
</SlideLayout>

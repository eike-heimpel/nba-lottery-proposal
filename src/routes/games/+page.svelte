<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';
</script>

<SlideLayout slideNumber="09">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">REGULAR SEASON</p>
		<h2 class="section-title mb-10">72 GAMES IS ENOUGH</h2>

		<div class="mb-8 grid gap-6 md:grid-cols-2">
			<!-- Current System -->
			<div class="rounded-lg border border-border bg-surface p-6 opacity-60">
				<h3 class="mb-4 font-heading text-sm font-600 tracking-wider text-text-dim uppercase">
					Current System
				</h3>
				<div class="space-y-3">
					<div class="flex items-baseline gap-3">
						<span class="font-heading text-4xl font-700 text-text-dim">82</span>
						<span class="text-sm text-text-dim">regular season games</span>
					</div>
					<div class="flex items-baseline gap-3">
						<span class="font-heading text-4xl font-700 text-text-dim">~20%</span>
						<span class="text-sm text-text-dim">games hit by load management</span>
					</div>
					<div class="flex items-baseline gap-3">
						<span class="font-heading text-4xl font-700 text-text-dim">0</span>
						<span class="text-sm text-text-dim">lottery tournament games</span>
					</div>
				</div>
			</div>

			<!-- Proposed System -->
			<div class="rounded-lg border-2 border-accent bg-surface p-6">
				<h3 class="mb-4 font-heading text-sm font-600 tracking-wider text-accent uppercase">
					Proposed System
				</h3>
				<div class="space-y-3">
					<div class="flex items-baseline gap-3">
						<span class="font-heading text-4xl font-700 text-text-bright">72</span>
						<span class="text-sm text-text">regular season games</span>
					</div>
					<div class="flex items-baseline gap-3">
						<span class="font-heading text-4xl font-700 text-text-bright">8</span>
						<span class="text-sm text-text">King of the Hill games (4 per conference)</span>
					</div>
					<div class="flex items-baseline gap-3">
						<span class="font-heading text-4xl font-700 text-text-bright">+</span>
						<span class="text-sm text-text">Play-in games (current format)</span>
					</div>
				</div>
			</div>
		</div>

		<div class="rounded-lg border border-yellow/30 bg-yellow/5 p-5">
			<h3 class="mb-2 font-heading text-sm font-600 tracking-wider text-yellow uppercase">
				WHY FEWER GAMES?
			</h3>
			<p class="text-sm leading-relaxed text-text-dim">
				Load management is sanctioned tanking — stars sitting out nationally televised games
				devalues the product. Fewer games means healthier players, higher intensity, better
				basketball. The King of the Hill and play-in add premium, high-stakes content that more than
				offsets lost regular season inventory.
			</p>
		</div>
	</div>
</SlideLayout>

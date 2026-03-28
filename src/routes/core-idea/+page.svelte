<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';

	const pillars = [
		{
			num: '01',
			title: 'Incentives, not rules',
			text: 'No salary floors or tanking penalties. The structure makes winning the smart play automatically.'
		},
		{
			num: '02',
			title: 'Self-enforcing',
			text: "You can't game a system where the optimal strategy at every position is to try to win."
		},
		{
			num: '03',
			title: 'More meaningful games',
			text: 'Every team has something to play for in March — and April. The dead zone is gone.'
		}
	];
</script>

<SlideLayout slideNumber="02">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">THE CORE IDEA</p>
		<h2 class="section-title mb-8">FLIP THE INCENTIVES</h2>

		<p class="mb-12 max-w-3xl text-xl font-light leading-relaxed text-text md:text-2xl">
			Don't give the best picks to the worst teams. Give the best odds to the team that <span
				class="font-semibold text-accent"
				>just barely missed the postseason</span
			>. Make winning the rational choice at every single position in the standings.
		</p>

		<div class="flex flex-col gap-5 md:flex-row">
			{#each pillars as pillar}
				<div class="flex-1 rounded-lg border border-border bg-surface p-6">
					<span class="mb-3 block font-heading text-4xl font-700 text-accent/20"
						>{pillar.num}</span
					>
					<h3 class="mb-2 font-heading text-base font-600 text-text-bright uppercase">
						{pillar.title}
					</h3>
					<p class="text-sm leading-relaxed text-text-dim">{pillar.text}</p>
				</div>
			{/each}
		</div>
	</div>
</SlideLayout>

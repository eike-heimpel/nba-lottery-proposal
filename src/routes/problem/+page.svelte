<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';

	const problems = [
		{
			title: 'Perverse Incentives',
			text: "The current draft rewards the worst teams with the best picks. Losing is the most efficient path to a franchise player. Front offices respond to incentives — and the incentives say lose."
		},
		{
			title: 'Multi-Year Teardowns',
			text: "'Trust the Process' proved you can gut a roster for 3-4 years and get rewarded. Fans watch meaningless basketball for seasons at a time while the front office collects assets."
		},
		{
			title: 'Dead Zone Basketball',
			text: "Teams between 25-35 wins have nothing to play for — too bad for playoffs, not bad enough for a top pick. March games become unwatchable for a third of the league."
		},
		{
			title: 'Bad Ownership Gets Bailed Out',
			text: "Owners who won't invest in coaching, development, or front offices get parachuted top picks anyway. The draft subsidizes dysfunction. Sacramento had high picks for a decade and stayed bad."
		}
	];
</script>

<SlideLayout slideNumber="01">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">THE PROBLEM</p>
		<h2 class="section-title mb-10">TANKING IS A RATIONAL STRATEGY</h2>

		<div class="grid gap-5 md:grid-cols-2">
			{#each problems as problem}
				<div class="rounded-lg border border-border bg-surface pl-5 border-l-3 border-l-accent">
					<div class="px-4 py-5">
						<h3 class="mb-2 font-heading text-lg font-600 text-text-bright">{problem.title}</h3>
						<p class="text-sm leading-relaxed text-text-dim">{problem.text}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</SlideLayout>

<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';

	const timeline = [
		{
			num: '1',
			timing: 'OCTOBER — APRIL',
			title: 'Regular Season',
			text: 'The standings determine your tier: playoffs, play-in, or lottery tournament. Every game matters because your final position decides what happens next.'
		},
		{
			num: '2',
			timing: 'MID-APRIL · ~10 DAYS, SIMULTANEOUS',
			title: 'Play-In + King of the Hill',
			text: 'Both run at the same time. The play-in determines the last playoff spots (current format). The KotH runs 4 games per conference — every game single-elimination, every game nationally televised.'
		},
		{
			num: '3',
			timing: 'LATE APRIL · DURING PLAYOFF ROUND 1',
			title: 'Lottery Draw — Prime Time',
			text: "Tournament results set each team's odds. The lottery balls drop during the first round of playoffs. Two spectacle events: first the tournament drama, then the lottery suspense."
		},
		{
			num: '4',
			timing: 'LATE APRIL — JUNE',
			title: 'Playoffs',
			text: '16 teams compete for the title. Standard format. Top seeds get a short rest during the play-in and King of the Hill window.'
		}
	];
</script>

<SlideLayout slideNumber="06">
	<div class="w-full max-w-4xl">
		<p class="section-label mb-3">SEASON FLOW</p>
		<h2 class="section-title mb-10">HOW THE YEAR PLAYS OUT</h2>

		<div class="relative pl-8">
			<div class="absolute left-[20px] top-0 h-full w-0.5 bg-border"></div>

			{#each timeline as item, i}
				<div class="relative mb-10 last:mb-0">
					<div
						class="absolute -left-8 flex h-[42px] w-[42px] items-center justify-center rounded-full font-heading text-lg font-700"
						style="background: {i === 0 ? 'var(--color-text-bright)' : i === 3 ? 'var(--color-warm-dim)' : 'var(--color-accent)'}; color: var(--color-bg)"
					>
						{item.num}
					</div>

					<div class="pl-8">
						<div class="mb-1 font-mono text-[11px] tracking-wider text-text-dim">{item.timing}</div>
						<h3 class="mb-2 font-heading text-xl font-600 text-text-bright uppercase">
							{item.title}
						</h3>
						<p class="text-sm leading-relaxed text-text-dim">{item.text}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</SlideLayout>

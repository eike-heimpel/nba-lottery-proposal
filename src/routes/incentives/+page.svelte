<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';

	const items = [
		{
			range: '1st–6th',
			title: 'Competing for a championship',
			text: 'Self-explanatory.',
			badge: 'WIN',
			highlight: false
		},
		{
			range: '7th–10th',
			title: 'Play-in + flat lottery odds',
			text: 'Fighting for playoff spots. The 4 eliminated teams get flat, identical lottery odds of 4.5% — zero draft incentive to slide. 7th and 8th seeds get a safety net. Just compete for the postseason.',
			badge: 'WIN',
			highlight: false
		},
		{
			range: '11th–15th',
			title: 'Regular season: higher finish = better tournament seed',
			text: 'Every position up means entering the King of the Hill later and needing fewer wins. 11th needs 1 win. 15th needs 4. Tanking in the regular season directly punishes you in the tournament.',
			badge: 'WIN',
			highlight: false
		},
		{
			range: '11th–15th',
			title: 'Tournament: every win improves your odds',
			text: 'Single elimination, win-or-go-home. Winning moves you up the odds ranking. Losing locks you in. This is real, desperate, meaningful basketball where both teams are trying their hardest.',
			badge: 'WIN',
			highlight: false
		},
		{
			range: '10th / 11th',
			title: 'The only soft spot',
			text: "The sharpest edge in the system. At 10th, you're in the play-in but need to win to make playoffs, and your consolation odds are flat 4.5%. At 11th, you enter the KotH as the top seed — win 1 game and you get the best lottery odds (11.5%). But players want postseason reps, coaches want playoff records, and any GM who publicly tanks out of a playoff tournament is taking a career risk. Every system has a weakest point. This one's is narrow and socially hard to exploit.",
			badge: 'NOTE',
			highlight: true
		}
	];
</script>

<SlideLayout slideNumber="08">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">INCENTIVE ANALYSIS</p>
		<h2 class="section-title mb-10">EVERY TEAM HAS A REASON TO WIN</h2>

		<div class="space-y-4">
			{#each items as item}
				<div class="flex flex-col gap-4 rounded-lg border border-border bg-surface p-5 md:flex-row">
					<div class="shrink-0 w-[110px]">
						<span class="font-heading text-lg text-accent">{item.range}</span>
						<div class="mt-0.5 font-mono text-[10px] text-text-dim">(per conf)</div>
					</div>
					<div class="flex-1">
						<div class="mb-1 flex flex-wrap items-center gap-3">
							<h3 class="font-heading text-base font-600 text-text-bright">{item.title}</h3>
							<span
								class="rounded px-2 py-0.5 font-mono text-[11px] font-500 {item.highlight
									? 'bg-warm/15 text-warm'
									: 'bg-text-bright/5 text-text-dim'}"
							>
								{item.badge}
							</span>
						</div>
						<p class="text-sm leading-relaxed text-text-dim">{item.text}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
</SlideLayout>

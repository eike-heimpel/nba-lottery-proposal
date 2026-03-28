<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';

	const objections = [
		{
			question: '"This punishes bad teams."',
			answer:
				"Good. It punishes bad management. Charlotte had 20 years of top picks and stayed irrelevant. Sacramento cycled through a decade of high selections and went nowhere. The current system doesn't produce competitive balance — it subsidizes dysfunction. This system demands professionalism. You still have lottery odds at the bottom. You just can't coast into the #1 pick by being the most negligent organization in the league."
		},
		{
			question: '"The 10th seed will tank into 11th."',
			answer:
				"This is the biggest gap in the system, and worth being honest about. But there are real forces working against it. Players and coaches have strong incentives to make the postseason — careers are built on playoff appearances, not lottery positioning. Tanking precisely into 11th is also harder than it sounds: you're not choosing between 10th and 11th, you're risking falling to 13th or 14th, where you need multiple KotH wins instead of one. The edge is narrow but real, and this is the likeliest place where the numbers need tweaking. But even untuned, the overall system is a massive improvement over rewarding teams for losing."
		},
		{
			question: '"How do bad teams actually get better?"',
			answer:
				"One step at a time. The current system is a slot machine — tank for years, pray for a generational pick, hope your franchise player doesn't leave. This system is a ramp. Improve from 15th to 13th, you enter KotH later and get better expected odds. Improve to 11th, you need one win for the best lottery odds. Every step up is rewarded. You build a team incrementally instead of burning it down and hoping."
		}
	];
</script>

<SlideLayout slideNumber="08">
	<div class="w-full max-w-5xl">
		<p class="section-label mb-3">OBJECTIONS</p>
		<h2 class="section-title mb-10">YES, WE THOUGHT ABOUT THAT</h2>

		<div class="space-y-6">
			{#each objections as obj}
				<div class="rounded-lg border border-border bg-surface p-6">
					<h3 class="mb-3 font-heading text-lg font-600 text-accent">{obj.question}</h3>
					<p class="text-sm leading-relaxed text-text-dim">{obj.answer}</p>
				</div>
			{/each}
		</div>
	</div>
</SlideLayout>

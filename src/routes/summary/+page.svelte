<script lang="ts">
	import SlideLayout from '$lib/components/SlideLayout.svelte';

	const points = [
		'<strong>Tanking is irrational</strong> at every position. In the regular season and in the tournament, winning always improves your situation.',
		'<strong>No new rules needed.</strong> Self-enforcing incentives. No salary floors, no tanking penalties, no committee reviews.',
		'<strong>King of the Hill</strong> turns the draft lottery into must-watch basketball — single-elimination games where bad teams play their hearts out.',
		'<strong>Two spectacle events:</strong> the tournament for competition and drama, the lottery draw for suspense and randomness.',
		'<strong>The dead zone is gone.</strong> Every team has meaningful basketball to play from October through April.',
		'<strong>Bad ownership is exposed</strong>, not bailed out. Finishing last and losing game 1 earns identical odds to a play-in team.'
	];
</script>

<SlideLayout
	slideNumber="08"
	background="linear-gradient(165deg, #0a0a0f 0%, #161622 50%, #0d0d15 100%)"
>
	<div
		class="pointer-events-none absolute bottom-[-200px] left-[-200px] h-[700px] w-[700px] rounded-full"
		style="background: radial-gradient(circle, rgba(196, 180, 154, 0.06) 0%, transparent 70%)"
	></div>

	<div class="relative z-10 w-full max-w-4xl">
		<p class="section-label mb-3">IN SUMMARY</p>
		<h2 class="section-title mb-10">A BETTER NBA</h2>

		<div class="mb-12 space-y-4">
			{#each points as point}
				<div class="flex gap-3">
					<span class="shrink-0 text-lg text-accent">✓</span>
					<p class="text-base leading-relaxed text-text-dim">{@html point}</p>
				</div>
			{/each}
		</div>

		<p class="text-lg text-text-dim">
			The NBA doesn't need more rules. <span class="font-semibold text-accent"
				>It needs better incentives.</span
			>
		</p>
	</div>
</SlideLayout>

<script lang="ts">
	interface Props {
		rank: string;
		title: string;
		description: string;
		tier: 'primary' | 'secondary' | 'accent';
	}

	let { rank, title, description, tier }: Props = $props();

	const tierStyles = {
		primary: { bg: 'var(--color-text-bright)', text: 'var(--color-bg)' },
		secondary: { bg: 'var(--color-warm)', text: 'var(--color-bg)' },
		accent: { bg: 'var(--color-accent)', text: '#fff' }
	};
</script>

<div class="flex flex-col border-border md:flex-row border-b last:border-b-0">
	<div
		class="flex min-w-[140px] items-center justify-center px-4 py-3 font-heading text-sm font-700 tracking-wider uppercase"
		style="background: {tierStyles[tier].bg}; color: {tierStyles[tier].text}"
	>
		{rank}
	</div>
	<div class="flex-1 px-5 py-4">
		<h3 class="mb-1 font-heading text-lg font-600 text-text-bright uppercase">{title}</h3>
		<p class="font-body text-sm leading-relaxed text-text-dim">{description}</p>
	</div>
</div>

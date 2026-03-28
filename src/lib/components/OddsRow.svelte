<script lang="ts">
	interface Props {
		label: string;
		pct: string;
		barWidth: number;
		emphasis: 'high' | 'mid' | 'low';
	}

	let { label, pct, barWidth, emphasis }: Props = $props();

	const barColors = {
		high: 'var(--color-accent)',
		mid: 'var(--color-warm)',
		low: 'var(--color-warm-dim)'
	};
</script>

<div class="flex items-center gap-3 py-1.5">
	<span class="w-[220px] shrink-0 font-mono text-[13px] text-text-dim">{label}</span>
	<span class="w-[60px] shrink-0 text-right font-heading text-[15px] font-500 text-text-bright"
		>{pct}</span
	>
	<div class="flex-1 rounded-full bg-surface-2 h-2.5">
		<div
			class="h-full rounded-full transition-all duration-500"
			style="width: {barWidth}%; background: {barColors[emphasis]}"
		></div>
	</div>
</div>

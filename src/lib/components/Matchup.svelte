<script lang="ts">
	interface Props {
		team1: string;
		team2: string;
	}

	let { team1, team2 }: Props = $props();
</script>

<div class="rounded-lg border border-border bg-surface px-5 py-3 text-center">
	<span class="font-heading text-base font-600 text-accent">{team1}</span>
	<span class="mx-3 font-mono text-xs text-text-dim">vs</span>
	<span class="font-heading text-base font-600 text-warm">{team2}</span>
</div>

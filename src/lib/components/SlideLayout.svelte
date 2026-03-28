<script lang="ts">
	import type { Snippet } from 'svelte';

	interface Props {
		slideNumber: string;
		background?: string;
		children: Snippet;
	}

	let { slideNumber, background = 'var(--color-bg)', children }: Props = $props();
</script>

<section
	class="relative flex min-h-dvh flex-col items-center px-5 py-16 md:justify-center md:px-20 md:py-15"
	style="background: {background}"
>
	<span class="slide-number">{slideNumber}</span>
	{@render children()}
</section>

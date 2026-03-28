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
	class="relative flex min-h-full flex-col items-center px-4 py-12 md:justify-center md:px-12 md:py-16"
	style="background: {background}"
>
	<span class="slide-number">{slideNumber}</span>
	{@render children()}
</section>

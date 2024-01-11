<script lang="ts">
	import Standard from './Standard.svelte';
	import StandardBoxed from './StandardBoxed.svelte';
</script>

<div class="logos">
	<div>
		<Standard />
	</div>
	<div>
		<StandardBoxed />
	</div>
	<div>
		<Standard filler={true} />
	</div>
	<div>
		<StandardBoxed filler={true} />
	</div>
</div>

<style>
	.logos {
		display: flex;
		gap: 4rem;
		padding: 2rem;
		align-items: center;
	}
</style>

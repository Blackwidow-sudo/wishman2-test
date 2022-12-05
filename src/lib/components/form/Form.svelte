<script lang="ts">
	import SubmitButton from '../btn/SubmitButton.svelte'

	/**
	 * Props.
	 */
	export let title: string
</script>

<form
	class="max-w-md"
	on:submit|preventDefault>
	<fieldset class="flex flex-col gap-2">
		<legend class="mb-4">
			<h2 class="text-3xl font-medium">{title}</h2>
		</legend>
		<slot name="fields" />
		<slot name="actions">
			<SubmitButton
				block
				center>Submit</SubmitButton>
		</slot>
	</fieldset>
</form>

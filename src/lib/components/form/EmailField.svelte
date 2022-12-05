<script lang="ts">
	export let id: string
	export let label: string
	export let value: string = ''
	export let placeholder: string = ''
</script>

<label for={id}>{label}</label>
<input
	class="px-3 py-2 shadow border rounded-md leading-tight"
	type="email"
	{id}
	{placeholder}
	bind:value />

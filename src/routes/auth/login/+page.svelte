<script lang="ts">
	import PageTransition from '$lib/components/PageTransition.svelte'

	const formData = {
		email: '',
		password: ''
	}

	function onSubmit() {}
</script>

<svelte:head>
	<title>Login</title>
</svelte:head>

<PageTransition>
	<form on:submit|preventDefault={onSubmit}>
		<input type="email" placeholder="Enter email" />
		<input type="password" placeholder="Enter password" />
		<input type="submit" value="Sign in" />
	</form>
</PageTransition>

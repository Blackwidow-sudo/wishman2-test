<script lang="ts">
	import SubmitButton from '$lib/components/btn/SubmitButton.svelte'
	import EmailField from '$lib/components/form/EmailField.svelte'
	import Form from '$lib/components/form/Form.svelte'
	import PasswordField from '$lib/components/form/PasswordField.svelte'
	import PageTransition from '$lib/components/PageTransition.svelte'

	const formData = {
		email: '',
		password: ''
	}

	function onSubmit() {
		alert(`{ email: ${formData.email}, password: ${formData.password} }`)
	}
</script>

<svelte:head>
	<title>Login</title>
</svelte:head>

<PageTransition>
	<div class="flex items-center justify-center">
		<Form
			title="Sign In"
			on:submit={onSubmit}>
			<svelte:fragment slot="fields">
				<EmailField
					id="email"
					label="Email:"
					placeholder="Enter email"
					bind:value={formData.email} />
				<PasswordField
					id="password"
					label="Password:"
					placeholder="Enter password"
					bind:value={formData.password} />
			</svelte:fragment>
		</Form>
	</div>
</PageTransition>

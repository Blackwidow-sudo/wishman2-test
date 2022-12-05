<script>
	import './app.scss'
	import { invalidate } from '$app/navigation'
	import { onMount } from 'svelte'
	import { supabaseClient } from '$lib/db'
	import Navbar from './Navbar.svelte'

	/**
	 * State & component variables.
	 */
	const pages = [
		{
			name: 'Home',
			href: '/'
		},
		{
			name: 'Login',
			href: '/auth/login'
		}
	]

	/**
	 * Lifecycle methods.
	 */
	onMount(() => {
		const {
			data: { subscription }
		} = supabaseClient.auth.onAuthStateChange(() => {
			invalidate('supabase:auth')
		})

		return () => {
			subscription.unsubscribe()
		}
	})
</script>

<Navbar {pages} />
<slot />

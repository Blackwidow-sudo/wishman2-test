<script lang="ts">
	import { page } from '$app/stores'

	/**
	 * Types.
	 */
	interface Page {
		name: string
		href: string
	}

	/**
	 * Props.
	 */
	export let pages: Page[]
</script>

<nav>
	<ul>
		{#each pages as { name, href }}
			<li>
				<a {href} class:active={$page.url.pathname === href}>{name}</a>
			</li>
		{/each}
	</ul>
</nav>

<style lang="scss">
	ul {
		list-style-type: none;
		display: flex;
		flex-direction: row;
		gap: 1rem;

		background-color: #f39ab7;
		padding: 0.5rem;
		margin: 0;

		li {
			background-color: #f5aac3;
			padding: 0.5rem 1rem;
		}

		li:hover {
			background-color: #c6889d;
		}

		a {
			text-decoration: none;
		}
	}

	.active {
		text-decoration: underline;
	}
</style>

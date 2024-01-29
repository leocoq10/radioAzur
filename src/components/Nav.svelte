<script>
	import { page } from '$app/stores';
	import Icon from '@iconify/svelte';
	import Side_menu from './Side_menu.svelte';

	let navs = [
		{
			title: 'Direct',
			href: '/live'
		},

		{
			title: 'Podcasts',
			href: '/podcasts'
		},

		{
			title: 'Actualites',
			href: '/actus'
		},

		{
			title: 'Programmes',
			href: '/programmes'
		}
	];

	let routeId;
	$: routeId = $page.route.id;

	let block;
	let show = false;

	function affiche() {
		show = !show;
	}

	$: block = show;
</script>

<nav>
	<button on:click={affiche} class="menu">
		{#if show}
			<Icon icon="material-symbols:close" />
		{:else}
			<Icon icon="material-symbols:menu" />
		{/if}
	</button>

	<div class="logo">
		<p>AZUR FM <span>98.5 FM</span></p>
	</div>
	<ul>
		{#each navs as { title, href }}
			<li><a {href} class:active={routeId === href} {title}>{title}</a></li>
		{/each}
	</ul>

	<div class="socialo">
		<div class="social-media">
			<a href="facebook.com"><Icon icon="ei:sc-facebook" /></a>
			<a href="twitter.com"><Icon icon="ei:sc-twitter" /></a>
			<a href="instagram.com"><Icon icon="ei:sc-instagram" /></a>
			<a href="youtube.com"><Icon icon="ei:sc-youtube" /></a>
			<a href="titktok.com"><Icon icon="ic:baseline-tiktok" /></a>
		</div>
		<button class="live-comp">
			<span class="p-50">Suivez le Direct</span>
			<Icon icon="ic:baseline-play-circle" height={25} />
		</button>
	</div>
</nav>

{#if show}
<slot>
	<Side_menu/>
</slot>
{/if}

<style>
	* {
		padding: 0;
		margin: 0;
		box-sizing: border-box;
	}

	nav {
		background-color: rgb(255, 255, 255);
		height: 80px;
		width: 100%;
		border-bottom: 1px solid whitesmoke;
		display: flex;
		justify-content: space-around;
		align-items: center;
		padding: 15px;
		box-shadow: 6px 6px 18px 0px rgba(0, 0, 0, 0.3);
	}

	ul {
		display: flex;
		gap: 30px;
		justify-content: center;
		align-items: center;
	}

	ul li {
		list-style: none;
	}

	ul li a {
		text-decoration: none;
		color: black;
		position: relative;
		padding-bottom: 5px;
	}

	ul li a::before {
		content: '';
		position: absolute;
		z-index: 100;
		bottom: -5px;
		left: 0;
		width: 0%;
		height: 3px;
		background: #396c94;
		transition: all 0.3s;
	}

	ul li a:hover::before {
		width: 100%;
	}

	.active {
		color: #086ec5;
	}

	.active:hover ul li a:hover::before {
		display: none;
	}

	.live-comp {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 5px;
		width: 165px;
		padding: 10px 5px;
		border-radius: 5px;
		background: #086ec5;
		color: white;
		font-weight: 600;
	}

	.social-media {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 10px;

		font-size: 20px;
	}

	.social-media a {
		background: #086ec5;
		padding: 5px;
		border-radius: 50%;
		color: white;
	}

	.logo p {
		font-size: 1.5rem;
		font-weight: 900;
		background: #086ec5;
		color: white;
		padding: 5px 0 5px 5px;
	}

	.logo p span {
		background-color: red;
		color: white;
		font-size: 1.5rem;
		font-weight: 900;
		padding: 9px;
	}

	.socialo {
		display: flex;
		justify-content: space-between;
		align-items: center;
		gap: 125px;
	}

	.menu {
		font-size: 25px;
		background: #086ec5;
		color: white;
		padding: 10px;
		border-radius: 5px;
	}

</style>

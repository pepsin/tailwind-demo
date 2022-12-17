<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/svelte-logo.svg';
	import github from '$lib/images/github.svg';
</script>

<header class="flex space-x-10">
	<div class="flex-none w-12 h-12 object-contain">
		<a href="https://kit.svelte.dev">
			<img src={logo} alt="SvelteKit" class="h-full w-full"/>
		</a>
	</div>

	<nav class="grow flex">
		<ul class="flex space-x-3 items-center">
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined} aria-selected={$page.url.pathname === '/'} class="aria-selected:bg-slate-50">
				<a href="/">Home</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
			<li aria-current={$page.url.pathname.startsWith('/sverdle') ? 'page' : undefined}>
				<a href="/sverdle">Sverdle</a>
			</li>
		</ul>
	</nav>

	<div class="flex-none">
		<a href="https://github.com/sveltejs/kit">
			<img src={github} alt="GitHub" />
		</a>
	</div>
</header>
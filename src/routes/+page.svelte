<script>
	import { onMount } from 'svelte';
	import Header from '../components/Header.svelte';
	import PostForm from '../components/PostForm.svelte';
	import PostsFeed from '../components/PostsFeed.svelte';

	onMount(() => {
		if (window != undefined) {
			if (!localStorage.getItem('lolanderid')) {
				window.location.href = '/login';
			}
		}
	});
</script>

<svelte:head>
	<script src="https://kit.fontawesome.com/2a7b093a26.js" crossorigin="anonymous"></script>
</svelte:head>

<div class="fixed w-full h-full">
	<Header />
	<PostsFeed />
	<PostForm />
</div>

<script context="module">
	export const prerender = true;
</script>

<script>
	// import Counter from '$lib/Counter.svelte';
	import News from '$lib/News.svelte';
</script>

<svelte:head>
	<title>Otranto Civic Club</title>
</svelte:head>

<section>
	<h1>
		<div class="welcome">
			<picture>
				<source srcset="svelte-welcome.webp" type="image/webp" />
				<img src="svelte-welcome.png" alt="Welcome" />
			</picture>
		</div>

		to the<br />Otranto Civic Club Homepage
	</h1>
	<img
		src="https://scontent.fcae1-1.fna.fbcdn.net/v/t1.18169-9/10361510_663300007115882_4031566852474803381_n.jpg?_nc_cat=110&ccb=1-5&_nc_sid=e3f864&_nc_ohc=tlDVSo2-paoAX9bliRc&_nc_ht=scontent.fcae1-1.fna&oh=00_AT-krghrW10sACa9g64YjVi7WQArLuiWQzDEQ0xUOAlKgQ&oe=626955C8"
		width="50%"
		alt="a sign"
	/>
	<p>----------------------------------------------------------------------------</p>

	<News />
	<!-- <Counter /> -->
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>

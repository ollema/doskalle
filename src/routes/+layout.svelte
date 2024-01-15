<script>
	import '../app.pcss';
	import '@fontsource/unifrakturcook';
</script>

<nav class="flex w-full items-center justify-center">
	<ul class="flex items-center gap-8 p-4 text-xl">
		<li class="hover:text-red-700 hover:underline">
			<a href="/logos">all logos</a>
		</li>
		<li class="hover:text-red-700 hover:underline">
			<a href="/logos/standard">with album art</a>
		</li>
	</ul>
</nav>

<div class="container">
	<slot />
</div>

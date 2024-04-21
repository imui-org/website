<script lang="ts">
	export let title: string;
	export let id: string;
	export let background: string;

	let sectionClasses = 'mx-auto px-4 py-16 sm:px-6 lg:px-8' + ' bg-' + background;
</script>

<section {id} class={sectionClasses}>
	<header class="text-center">
		<h2 class="text-4xl font-bold text-gray-900 sm:text-3xl lg:text-4xl mb-8">{title}</h2>
	</header>
	<div class="mx-auto max-w-screen-xl">
		<slot></slot>
	</div>
</section>

<script lang="ts">
	export let title: string;
	export let subtitle: string;
</script>

<article class="overflow-hidden rounded-lg shadow transition hover:shadow-lg">
	<slot></slot>
	<div class="bg-white p-4 sm:p-6">
		<h3 class="text-lg font-medium text-gray-900">
			{title}
		</h3>
		<p class="mt-2 line-clamp-3 text-sm/relaxed text-gray-500">
			{subtitle}
		</p>
		<a href="#" class="group mt-4 inline-flex items-center gap-1 text-sm font-medium text-blue-600">
			Mehr lesen
			<span aria-hidden="true" class="block transition-all group-hover:ms-0.5 rtl:rotate-180">
				&rarr;
			</span>
		</a>
	</div>
</article>

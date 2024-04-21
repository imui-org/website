<script lang="ts">
	import ProjectCard from './ProjectCard.svelte';
	import loopBlocksImage from '$lib/assets/images/projects/loopblocks.webp';
	import melodyBlocksImage from '$lib/assets/images/projects/melodyblocks.webp';

	const columnClass = 'flex flex-wrap content-start px-5 w-full sm:w-1/2';
	const innerItems = 'w-full flex-initial pb-5';

	enum MediaClass {
		Image,
		Vimeo
	}

	let projects = [
		{
			title: 'LoopBlocks',
			subtitle: 'Rhythmen bauen – Beats stecken',
			mediaSrc: loopBlocksImage,
			mediaClass: MediaClass.Image
		},
		{
			title: 'MelodyBlocks',
			subtitle: 'Melodien konstruieren',
			mediaSrc: melodyBlocksImage,
			mediaClass: MediaClass.Image
		},
		{
			title: 'SnoeSky',
			subtitle: 'Der Klang der Sterne',
			mediaSrc: 'https://player.vimeo.com/video/412368397',
			mediaClass: MediaClass.Vimeo
		},
		{
			title: 'SonicDive',
			subtitle: 'Eintauchen - Abtauchen',
			mediaSrc: 'https://player.vimeo.com/video/423651377',
			mediaClass: MediaClass.Vimeo
		}
	];
</script>

<div class="flex flex-wrap justify-center">
	{#each { length: 2 } as _, i}
		<div class={columnClass}>
			{#each projects.slice(i * (projects.length / 2), (i + 1) * (projects.length / 2)) as { title, subtitle, mediaSrc, mediaClass }}
				<div class={innerItems}>
					<ProjectCard {title} {subtitle}>
						{#if mediaClass == MediaClass.Image}
							<img alt={title} src={mediaSrc} class="w-full object-cover" />
						{:else if mediaClass == MediaClass.Vimeo}
							<iframe
								src={mediaSrc}
								{title}
								class="aspect-video w-full"
								allow="autoplay; fullscreen; picture-in-picture"
								allowfullscreen={true}
							></iframe>
						{:else}{/if}
					</ProjectCard>
				</div>
			{/each}
		</div>
	{/each}
</div>

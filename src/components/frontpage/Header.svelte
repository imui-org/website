<script lang="ts">
	import { particlesInit } from '@tsparticles/svelte';
	import { loadSlim } from '@tsparticles/slim';
	import { type IOptions, type RecursivePartial } from '@tsparticles/engine';
	import { onMount } from 'svelte';

	export let navigationItems: {
		name: string;
		href: string;
	}[] = [];

	let ParticlesComponent: ConstructorOfATypedSvelteComponent;

	onMount(async () => {
		const module = await import('@tsparticles/svelte');

		ParticlesComponent = module.default;
	});

	let particlesConfig: RecursivePartial<IOptions> = {
		clear: true,
		fullScreen: { enable: false, zIndex: 0 },
		detectRetina: true,
		fpsLimit: 60,
		interactivity: {
			detectsOn: 'canvas',
			events: {
				onClick: { enable: true, mode: 'repulse' },
				onHover: {
					enable: true,
					mode: 'bubble',
					parallax: { enable: false, force: 2, smooth: 10 }
				}
			},
			modes: {
				bubble: {
					distance: 250,
					duration: 2,
					mix: false,
					opacity: 0,
					size: 0,
					divs: { distance: 200, duration: 0.4, mix: false }
				},
				repulse: {
					distance: 400,
					duration: 0.4,
					factor: 100,
					speed: 1,
					maxSpeed: 50,
					easing: 'ease-out-quad',
					divs: {
						distance: 200,
						duration: 0.4,
						factor: 100,
						speed: 1,
						maxSpeed: 50,
						easing: 'ease-out-quad',
						selectors: {}
					}
				}
			}
		},
		particles: {
			color: {
				value: '#ffffff'
			},
			move: {
				attract: { distance: 200, enable: false, rotate: { x: 3000, y: 3000 } },
				center: { x: 50, y: 50, mode: 'percent', radius: 0 },
				enable: true,
				speed: { min: 0.1, max: 1 }
			},
			number: {
				density: { enable: true },
				value: 160
			},
			opacity: {
				value: { min: 0.1, max: 1 },
				animation: {
					enable: true,
					speed: 1
				}
			},
			shape: { type: 'circle' },
			size: {
				value: { min: 1, max: 3 }
			}
		}
	};

	void particlesInit(async (engine) => {
		await loadSlim(engine);
	});
</script>

<header class="h-screen flex flex-col bg-white">
	<div
		class="bg-white mx-auto max-w-screen-xl px-4 sm:px-6 lg:px-8 flex h-16 items-center justify-between"
	>
		<!-- Logo on the left -->
		<div class="md:flex md:items-center md:gap-12"></div>
		<!-- Main menu -->
		<div class="hidden md:block">
			<nav aria-label="Main navigation">
				<ul class="flex items-center gap-6 text-sm">
					{#each navigationItems as { name, href }}
						<li>
							<a class="text-xl text-gray-900 transition hover:text-gray-500/75" href={href}>{name}</a>
						</li>
					{/each}
				</ul>
			</nav>
		</div>
		<!-- Right side -->
		<div class="flex items-center gap-4">
			<div class="block md:hidden">
				<button class="rounded bg-gray-100 p-2 text-gray-600 transition hover:text-gray-600/75">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-5 w-5"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						stroke-width="2"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16"></path>
					</svg>
				</button>
			</div>
		</div>
	</div>
	<div
		class="relative bg-gradient-to-r from-teal-400 to-teal-500 flex-1 flex items-center justify-center"
	>
		<svelte:component
			this={ParticlesComponent}
			id="tsparticles"
			class="absolute inset-0"
			options={particlesConfig}
		/>

		<div class="mx-auto max-w-screen-xl px-4 py-32 lg:flex lg:items-center">
			<div class="mx-auto max-w-xl text-center">
				<div class="px-20 mb-2">
					<h1
						class="text-5xl text-white font-extrabold drop-shadow sm:text-7xl rounded-lg border-solid border-white border-4 pt-5 pb-4"
					>
						imui
					</h1>
				</div>
				<h2>
					<strong class="text-2xl drop-shadow font-extrabold text-white sm:block"
						>Verein für inklusive Musikinstrumente</strong
					>
				</h2>
			</div>
		</div>
	</div>
</header>

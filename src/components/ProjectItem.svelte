<script lang="ts">
	type TechnologyKeys =
		| 'typescript'
		| 'svelte'
		| 'tailwind'
		| 'postgres'
		| 'prisma'
		| 'openai'
		| 'go';

	const TechnologiesTable: Record<
		TechnologyKeys,
		{
			src: string;
			height: number;
			alt: string;
		}
	> = {
		typescript: {
			src: '/typescript.png',
			height: 25,
			alt: 'TypeScript'
		},
		svelte: {
			src: '/svelte.png',
			height: 25,
			alt: 'SvelteKit'
		},
		tailwind: {
			src: '/tailwind.png',
			height: 15,
			alt: 'Tailwind CSS'
		},
		postgres: {
			src: '/postgres.png',
			height: 25,
			alt: 'PostgreSQL'
		},
		prisma: {
			src: '/prisma.png',
			height: 25,
			alt: 'Prisma'
		},
		openai: {
			src: '/openai.png',
			height: 25,
			alt: 'OpenAI'
		},
		go: {
			src: '/go.png',
			height: 20,
			alt: 'Go'
		}
	};

	export let label: string;
	export let technologies: TechnologyKeys[];
	export let url: string;
</script>

<div class="flex flex-col gap-4 md:flex-row md:gap-8">
	<div class="flex flex-col gap-4 md:w-[200px]">
		<a href={url} target="_blank" class="whitespace-nowrap hover:underline">{label}</a>
		<div class="flex flex-wrap items-center gap-3">
			{#each technologies as technology}
				<div class="group relative cursor-pointer">
					<img
						class="opacity-40 transition-all group-hover:scale-[125%] group-hover:opacity-100"
						style={`height: ${TechnologiesTable[technology].height}px`}
						src={TechnologiesTable[technology].src}
						alt={TechnologiesTable[technology].alt}
					/>
					<div
						class="pointer-events-none absolute -bottom-[40px] right-1/2 z-10 translate-x-1/2 whitespace-nowrap rounded-full bg-[#171717] p-1 px-2 text-xs text-[#898989] opacity-0 transition-opacity group-hover:opacity-100"
					>
						{TechnologiesTable[technology].alt}
					</div>
				</div>
			{/each}
		</div>
	</div>
	<p class="flex-1 font-light">
		<slot />
	</p>
</div>

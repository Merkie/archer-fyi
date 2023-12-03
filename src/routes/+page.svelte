<script lang="ts">
	import DividerWithLabel from '~/components/DividerWithLabel.svelte';
	import ProjectItem from '~/components/ProjectItem.svelte';
</script>

<svelte:head>
	<title>Archer Calder</title>
</svelte:head>

<main class="flex min-h-screen flex-col items-center pb-28 pt-12 md:pt-28">
	<div class="flex w-[80%] max-w-[750px] flex-col">
		<div class="flex flex-col gap-8 md:flex-row md:gap-16">
			<div class="flex flex-col">
				<p>Archer Calder</p>
				<p class="mb-4 whitespace-nowrap text-sm text-[#434343]">Full-Stack Web Developer</p>
				<a
					href="https://github.com/Merkie"
					target="_blank"
					class="w-fit border-b border-black text-sm hover:border-white"
				>
					<i class="bi bi-github"></i>
					<span class="mr-2">Github</span>
					<i class="bi bi-box-arrow-up-right"></i>
				</a>
				<a
					href="https://linkedin.com/in/archer-calder/"
					target="_blank"
					class="mt-1 w-fit border-b border-black text-sm hover:border-white"
				>
					<i class="bi bi-linkedin"></i>
					<span class="mr-2">LinkedIn</span>
					<i class="bi bi-box-arrow-up-right"></i>
				</a>
			</div>
			<div class="flex flex-col gap-2 font-light">
				<p>
					Hey there 👋 I'm a full-stack web developer from Houston. I'm currently working at <a
						href="https://drinkflowater.com/"
						class="underline"
						target="_blank">FloWater</a
					>, developing the next generation of AI-powered marketing tools.
				</p>
				<p>
					I created and maintain <a
						href="https://www.freespeechaac.com/"
						class="underline"
						target="_blank">FreeSpeech</a
					>, an open-source augmentative and alternative communication (AAC) web application for
					people who are non-verbal.
				</p>
			</div>
		</div>
		<DividerWithLabel label={'Media'}>
			<div class="flex items-center justify-between">
				<a
					href="https://www.cnn.com/2021/12/19/us/texas-teen-freespeech-app/index.html"
					target="_blank"
					class="opacity-40 transition-opacity hover:opacity-100"
				>
					<img class="h-[30px] sm:h-[40px] md:h-[50px]" src="/cnn.png" alt="CNN" />
				</a>
				<a
					href="https://www.bbc.com/news/av/disability-57515272"
					target="_blank"
					class="opacity-40 transition-opacity hover:opacity-100"
				>
					<img class="h-[30px] sm:h-[40px] md:h-[50px]" src="/bbc.png" alt="BBC" />
				</a>
				<div class="relative">
					<img class="h-[30px] opacity-40 sm:h-[40px] md:h-[50px]" src="/github.png" alt="GitHub" />
					<div
						class="absolute bottom-0 right-0 translate-x-1/2 translate-y-1/2 scale-75 rounded-full bg-[#171717] p-1 px-2 text-xs text-[#898989] md:scale-100"
					>
						Soon
					</div>
				</div>
			</div>
		</DividerWithLabel>
		<DividerWithLabel label={'Projects'}>
			<div class="flex flex-col gap-12 md:gap-8">
				<ProjectItem
					label={'FreeSpeech'}
					technologies={['typescript', 'svelte', 'tailwind', 'postgres', 'prisma']}
				>
					FreeSpeech is an open-source augmentative and alternative communication (AAC) web
					application for people who are non-verbal.
				</ProjectItem>
				<ProjectItem
					label={'GPT Cold Email'}
					technologies={['openai', 'typescript', 'svelte', 'tailwind', 'postgres', 'prisma']}
				>
					GPT Cold Email is an open-source web application that generates and sends cold emails
					using OpenAI's suite of language models and standard SMTP requests.
				</ProjectItem>
				<ProjectItem label={'UULE'} technologies={['go']}>
					UULE is an open-source Go package that generates Google's UULE parameter for
					programmatically searching Google from a specific location.
				</ProjectItem>
				<ProjectItem label={'BrightData SDK'} technologies={['go']}>
					BrightData SDK is an open-source Go package that provides a simple interface for
					programmatically using BrightData's proxies and APIs.
				</ProjectItem>
			</div>
		</DividerWithLabel>
	</div>
</main>

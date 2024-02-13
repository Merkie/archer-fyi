<script lang="ts">
	import DividerWithLabel from '~/components/DividerWithLabel.svelte';
	import ProjectItem from '~/components/ProjectItem.svelte';
	import NewsLink from '~/components/NewsLink.svelte';
</script>

<svelte:head>
	<title>Archer Calder</title>
</svelte:head>

<main class="flex min-h-screen flex-col items-center pb-28 pt-12 md:pt-28">
	<div class="flex w-[80%] max-w-[750px] flex-col">
		<div class="flex flex-col gap-8 md:flex-row md:gap-16">
			<div class="flex flex-col">
				<img src="/me.png" class="mb-4 max-w-[200px] rounded-full" alt="" />
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
					Hey there 👋 I'm Archer, a passionate full-stack web developer based in Houston. At <a
						href="https://huzi.ai/?auth=Login"
						class="underline"
						target="_blank">Huzi</a
					>, I'm at the forefront of developing the next generation of AI-powered real estate
					software, aimed at optimizing transactions, enhancing property and market analysis, and
					simplifying property management.
				</p>

				<p>
					I created and maintain <a
						href="https://www.freespeechaac.com/"
						class="underline"
						target="_blank">FreeSpeech</a
					>, an open-source augmentative and alternative communication (AAC) web application for
					people who are non-verbal. (I also have a few more open-source projects I maintain and
					contribute to)
				</p>
			</div>
		</div>
		<DividerWithLabel label={'Published Media'}>
			<div class="flex flex-col gap-8">
				<NewsLink
					href={'https://github.com/readme/featured/open-source-aac'}
					title={'Coding accessibility: How Della found her voice with open source AAC '}
					site={'github'}
					date={'Dec 3, 2023'}
					author={'Mike Melanson'}
				/>
				<NewsLink
					href={'https://www.cnn.com/2021/12/19/us/texas-teen-freespeech-app/index.html'}
					title={'A Texas teen couldn’t speak with his sister, so he created an app to give her a voice'}
					site={'cnn'}
					date={'Dec 19, 2021'}
					author={'Sophie Tremblay'}
				/>
				<NewsLink
					href={'https://www.bbc.com/news/av/disability-57515272'}
					title={'How a US teen developed an app to help his sister talk'}
					site={'bbc'}
					date={'Jun 30, 2021'}
					author={'Harry Bligh and Dianne King'}
				/>
			</div>
		</DividerWithLabel>
		<DividerWithLabel label={'Projects'}>
			<div class="flex flex-col gap-12 md:gap-8">
				<ProjectItem
					label={'FreeSpeech'}
					url={'https://github.com/Merkie/freespeech'}
					technologies={['typescript', 'svelte', 'tailwind', 'postgres', 'prisma']}
				>
					FreeSpeech is an open-source augmentative and alternative communication (AAC) web
					application for people who are non-verbal.
				</ProjectItem>
				<ProjectItem
					label={'GPT Cold Email'}
					url={'https://github.com/Merkie/gpt-cold-email'}
					technologies={['openai', 'typescript', 'svelte', 'tailwind', 'postgres', 'prisma']}
				>
					GPT Cold Email is an open-source web application that generates and sends cold emails
					using OpenAI's suite of language models and standard SMTP requests.
				</ProjectItem>
				<ProjectItem
					url={'https://pkg.go.dev/github.com/merkie/uule-go'}
					label={'UULE'}
					technologies={['go']}
				>
					UULE is an open-source Go package that generates Google's UULE parameter for
					programmatically searching Google from a specific location.
				</ProjectItem>
				<ProjectItem
					url={'https://pkg.go.dev/github.com/merkie/brightdata-sdk-go'}
					label={'BrightData SDK'}
					technologies={['go']}
				>
					BrightData SDK is an open-source Go package that provides a simple interface for
					programmatically using BrightData's proxies and APIs.
				</ProjectItem>
			</div>
		</DividerWithLabel>
	</div>
</main>

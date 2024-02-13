<script lang="ts">
	export let href: string;
	export let title: string;
	export let site: string;
	export let date: string;
	export let author: string;
</script>

<a
	{href}
	target="_blank"
	class="relative flex items-center gap-8 rounded-lg border p-8 opacity-40 transition-opacity hover:opacity-100"
>
	<img class="h-[30px] sm:h-[40px] md:h-[50px]" src={`/${site}.png`} alt={`${site} logo`} />
	<p class="text-xl">
		{`${title} `}<i class="bi bi-box-arrow-up-right ml-2"></i>
	</p>
	<div
		class="absolute bottom-0 right-4 flex translate-y-1/2 items-end gap-4 font-mono text-xs text-white"
	>
		<div class="rounded-lg border border-white bg-black p-1 px-2">{author}</div>
		<div class="rounded-lg border border-white bg-black p-1 px-2">
			{date}
		</div>
	</div>
</a>

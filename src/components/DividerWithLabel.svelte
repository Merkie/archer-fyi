<script lang="ts">
	export let label: string;
</script>

<div class="relative mt-16 border-t border-[#171717] pt-8">
	<div class="absolute left-0 top-0 -translate-y-1/2 bg-black pr-4">
		<p class="text-sm font-light text-[#434343]">
			{label}
		</p>
	</div>
	<slot />
</div>

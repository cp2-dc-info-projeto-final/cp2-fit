<script lang="ts">
  import { Heading } from 'flowbite-svelte';
  import Menu from '../components/Menu.svelte';
  import {  P, ImagePlaceholder, Skeleton, TextPlaceholder } from "flowbite-svelte";
</script>

<Menu />

<div class="text-center p-8 pt-32">
	<Heading tag="h2" class="text-4xl font-extrabold tracking-tight text-gray-900 dark:text-white mb-6">Menu</Heading>
	<P class="text-lg leading-relaxed text-gray-700 dark:text-gray-300 mb-4 text-justify">
		Lorem 
	</P>
	<Skeleton class="mt-16 mb-8" />
	<ImagePlaceholder class="my-8" />
	<TextPlaceholder class="my-8" />
</div>
<script lang="ts">
	import imgBg from '../assets/bg2.png';
	import imgMoto from '../assets/bgg3.png';
	import Card from '../component/card.svelte';
	import { arraytitle } from '../store';
	import Icon from '@iconify/svelte';
</script>

<div class="container mx-auto min-w-fit md:max-h-screen">
	<div class="grid items-end grid-rows-2 gap-2 justify-items-center md:grid-cols-2">
		<div class=" min-w-fit md:min-h-screen md:mt-5">
			<img
				src={imgBg}
				class="h-auto max-w-sm transition-shadow duration-300 ease-in-out rounded-lg shadow-none md:max-w-lg lg:max-w-xl"
				alt="icon_nav"
			/>
		</div>
		<div class="flex items-center pb-20 min-w-fit md:pb-0 md:min-h-screen md:mb-0">
			<div class="grid content-end grid-rows-2 gap-5 justify-items-center">
				<div class=" md:-mb-15">
					<img
						src={imgMoto}
						class="h-auto max-w-sm transition-shadow duration-300 ease-in-out rounded-lg shadow-none md:max-w-md lg:max-w-lg"
						alt="icon_grid"
					/>
				</div>
				<div>
					<button type="button" class="btn bg-gradient-to-br variant-filled-surface"
						>Enroll now !!!</button
					>
				</div>
			</div>
		</div>
	</div>
</div>
<div class="flex flex-col max-w-full md:max-h-screen">
	<div class="pb-8 text-center basis-full">
		<h1 class="text-3xl font-bold leading-7 text-surface-600 font_gelaso">
			Apa keuntungan bekerja sama dengan kami ?
		</h1>
	</div>
	<div class="ml-10 mr-10 basis-full">
		<div class="grid gap-2 text-center md:gap-4 md:grid-cols-2 md:grid-flow-row lg:grid-cols-3">
			{#each $arraytitle as item}
				<div>
					<Card>
						<span slot="theader">
							<button type="button" class="btn-icon btn-icon-xl variant-soft-surface"
								><Icon icon={item.iconset} style="font-size: 35px" /></button
							>
							<div class="bg-yellow-200 rounded-full" />
						</span>
						<span slot="tcontent">
							<h2 class="text-xl font-bold leading-10 font_gelaso text-surface-600">
								{item.title}
							</h2>
						</span>
						<span slot="tfooter">
							<h2 class="text-lg leading-tight font_gelaso text-surface-600">
								{item.titleFooter}
							</h2>
						</span>
					</Card>
				</div>
			{/each}
		</div>
	</div>
</div>
<div class="flex flex-col max-w-full max-h-screen pt-10 bg-yellow-200">
	<div class="text-center basis-full">
		<h1 class="text-3xl font-bold leading-7 text-surface-600 font_gelaso">
			berikutdaftar harga pengerjaan software
		</h1>
	</div>
</div>

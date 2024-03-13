<script lang="ts">
	
	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';
	import { Stepper, Step } from '@skeletonlabs/skeleton';
	import { TabGroup, Tab, TabAnchor } from '@skeletonlabs/skeleton';
	
	import logo from '../lib/assets/с2сpay320.png'
	import brc from '../lib/assets/c2cpaybrc.png'

	let tabSet: number = 0;
</script>

<main>

	<div class="container mx-auto flex justify-center items-center">
		<margin>
			<figure>
				<section class="img-bg" />
				<img alt="C2C-PAY" src="{logo}" />
			</figure>
		</margin>
	</div>

	<div class="container mx-auto flex justify-center items-center">
		<div class="h4">		
			Добро пожаловать!  
		</div>
	</div>
	<div class="container mx-auto flex justify-center items-center">

		<div class="h4">		
			Скоро открытие 
		</div>
	
	</div>

	<div class="container mx-auto flex">
		<div class="space-y-2">
			<space>
				<div class="h3">
					О компании			 	
				</div>
			</space>
	
			<p>Компания C2C PAY (PWT) LTD основана в 2024 году на острове Шри-Ланка.</p>
			<Accordion>
	
				<AccordionItem>
					<!--<svelte:fragment slot="lead">(icon)</svelte:fragment> -->
					<svelte:fragment slot="summary">Свидетельство о регистрации компании в Демократической Социалистической Республике Шри-Ланка</svelte:fragment>
					<svelte:fragment slot="content">
						<div class="container h-full mx-auto flex justify-center items-center">
							<div class="space-y-5">
								<img alt="C2C-PAY" src="{brc}" />
							</div>
						</div>
						
					</svelte:fragment>
				</AccordionItem>
				<AccordionItem>
					<!--<svelte:fragment slot="lead">(icon)</svelte:fragment> -->
					<svelte:fragment slot="summary">Контактная информация:</svelte:fragment>
					<svelte:fragment slot="content">
						<div class="container h-full mx-auto flex justify-center items-center">
							<div class="space-y-5">
								<p>Юридический адрес: 80280, Sri Lanka, Galle, Paluwaththa, Piyadigama, Gintota</p>
								<p>Электронная почта: c2cpayinfo@gmail.com</p>	
								<p>Телефон для связи: +94 7612 44 814</p>									
							</div>
						</div>
						
					</svelte:fragment>
				</AccordionItem>
			
			</Accordion>
			<p>Основной вид деятельности: разработка корпоративного программного обеспечения.</p>
			<p>Основной продукт: цифровой склад именных ценных бумаг.</p>
		</div>

	</div>
	
</main>

<style lang="postcss">
	main {
		max-width: 960px;
		margin: 40px;
		align-content: center;
	}
	space {
		margin: 20px;
	}
	space-big {
		margin-top: 150px;
		margin-bottom: 150px;
	}
	margin {
		margin-top: 150px;
		margin-bottom: 150px;
		align-content: center;
	}


	figure {
		@apply flex relative flex-col;
	}
	figure svg,
	.img-bg {
		@apply w-64 h-64 md:w-80 md:h-80;
	}
	.img-bg {
		@apply absolute z-[-1] rounded-full blur-[50px] transition-all;
		animation: pulse 5s cubic-bezier(0, 0, 0, 0.5) infinite,
			glow 5s linear infinite;
	}
	@keyframes glow {
		0% {
			@apply bg-primary-400/50;
		}
		33% {
			@apply bg-secondary-400/50;
		}
		66% {
			@apply bg-tertiary-400/50;
		}
		100% {
			@apply bg-primary-400/50;
		}
	}
	@keyframes pulse {
		50% {
			transform: scale(1.5);
		}
	}
</style>
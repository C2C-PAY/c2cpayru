<script lang="ts">
	import '../app.postcss';

	// Highlight JS
	import hljs from 'highlight.js/lib/core';
	import 'highlight.js/styles/github-dark.css';
	import { storeHighlightJs } from '@skeletonlabs/skeleton';
	import xml from 'highlight.js/lib/languages/xml'; // for HTML
	import css from 'highlight.js/lib/languages/css';
	import javascript from 'highlight.js/lib/languages/javascript';
	import typescript from 'highlight.js/lib/languages/typescript';

	hljs.registerLanguage('xml', xml); // for HTML
	hljs.registerLanguage('css', css);
	hljs.registerLanguage('javascript', javascript);
	hljs.registerLanguage('typescript', typescript);
	storeHighlightJs.set(hljs);

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });

        // Skeleton
	import { AppShell } from '@skeletonlabs/skeleton';
	import { AppBar } from '@skeletonlabs/skeleton';
	import { LightSwitch } from '@skeletonlabs/skeleton';


	import logo from '../lib/assets/с2сpay64.png'
</script>

<AppShell>
	<svelte:fragment slot="header">
		<AppBar>
			<svelte:fragment slot="lead">
				<div class="space-y-5">
					<img alt="C2C-PAY" src="{logo}" />
				</div>
			</svelte:fragment>

			<h2 class="h2" id="greetings">
				Великолепное путешествие с финансовой независимостью
			</h2>

			<svelte:fragment slot="trail">
				<LightSwitch />
			</svelte:fragment>
			<svelte:fragment slot="headline">
				<h3 class="h3">
					Для сохранности денежных средств в путешествиях по миру пользуйтесь C2C PAY и наслаждайтесь главным, а мы позаботимся об оплате счетов
				</h3>				
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>

	<!-- <svelte:fragment slot="pageHeader">Page Header</svelte:fragment> -->
	
	<!-- <svelte:fragment slot="sidebarLeft">Sidebar Left</svelte:fragment> -->
	<!-- <svelte:fragment slot="sidebarRight">Sidebar Right</svelte:fragment> -->
	<!--  -->
	<!-- Router Slot -->
	<div class="container h-full mx-auto flex justify-center items-center">
		<slot />
	</div>

	
	<!-- ---- / ---- -->
	<!-- <svelte:fragment slot="pageFooter">Page Footer</svelte:fragment> -->
	<svelte:fragment slot="footer">
		<AppBar>
			<svelte:fragment slot="lead">
				<div class="container h-full mx-auto flex justify-center items-center">
					<h7 class="h7">
						Copyright 2024 C2C PAY (PWT) LTD
					</h7>	
				</div>
			</svelte:fragment>


			<svelte:fragment slot="trail">
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://github.com/C2C-PAY/c2cpayru"
					target="_blank"
					rel="noreferrer"
				>
					GitHub
				</a>
			</svelte:fragment>
		</AppBar>

	</svelte:fragment>
</AppShell>
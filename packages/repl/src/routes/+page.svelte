<script lang="ts">
	import Repl from '$lib/Repl.svelte';
	import { onMount } from 'svelte';
	import '@sveltejs/site-kit/styles/index.css';

	let repl: ReturnType<typeof Repl>;

	onMount(() => {
		repl.set({
			files: [
				{
					type: 'file',
					name: 'App.svelte',
					basename: 'App.svelte',
					contents:
						'<script>\n\tlet count = $state(0);\n\n\tfunction increment() {\n\t\tcount += 1;\n\t}\n</scr' +
						'ipt>\n\n<button onclick={increment}>\n\tclicks: {count}\n</button>',
					text: true,
				}
			]
		});
	});
</script>

<main>
	<Repl bind:this={repl} />
</main>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
	}

	main {
		height: 100vh;
	}

	:global .ͼo {
		color: #cba6f7;
	}

	:global .ͼq {
		color: #89b4fa;
	}

	:global .ͼt {
		color: #89b4fa;
	}

	:global .ͼp{
		color: #f9e2af;
	}

	:global .ͼu{
		color: #cdd6f4;
	}

	:global .ͼv{
		color: #9399b2;
	}

	:global .ͼs{
		color: #cdd6f4;
	}

	:global .error{
		background-color: #11111b !important;
	}

	:global .cm-line{
		color: #cdd6f4;
	}

	@font-face {
		font-family: "CaskaydiaCoveNF";
		src: url("/fonts/CaskCov.woff2");
	}

	:global .cm-editor{
		font-family: "CaskaydiaCoveNF" !important;
	}

	:global .cm-gutters{
		font-family: "CaskaydiaCoveNF" !important;
		background-color: #1e1e2e !important;
		color: #cdd6f4 !important;
	}

	:global .button{
		color: #cdd6f4 !important;
		font-family: "CaskaydiaCoveNF" !important;
	}

	:global .drag-handle{
		color: #cdd6f4 !important;
	}

	:global .container{
		color: #181825 !important;
	}

	:global pre{
		color: #cdd6f4 !important;
	}

	:global .overlay{
		background-color: #6c7086 !important;
		
	}

	:global .cm-content{
		font-family: "CaskaydiaCoveNF" !important;
	}

	:global :root{
		font-family: "CaskaydiaCoveNF" !important;
	}

	:global .dropdown{
		color: #cdd6f4 !important;
		font-family: "CaskaydiaCoveNF" !important;
	}

	:global .cm-layer{
		color: #6c7086 !important;
	}

	:global .view-toggle{
		color: #cdd6f4 !important;
	}

	:global .filename{
		font-family: "CaskaydiaCoveNF" !important;
	}

	:global body{
		font-family: "CaskaydiaCoveNF" !important;
	}

	:global input{
		font-family: "CaskaydiaCoveNF" !important;
	}

	:global .ast-view{
		background-color: #1e1e2e !important;	
		font-family: "CaskaydiaCoveNF" !important;
	}

	:global .panel-body{
		font-family: "CaskaydiaCoveNF" !important;
		color: #cdd6f4 !important;
	}

	:global .panel-header{
		font-family: "CaskaydiaCoveNF" !important;
		color: #cdd6f4 !important;
	}
</style>

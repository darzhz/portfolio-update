<script>
	import IconPlacer from "./IconPlacer.svelte";
	let images = ["javascript","svelte","nodejs-icon","css-3","mongodb","express","figma","java","processing","mysql","git-icon","vitejs"];
</script>
<div id="container">
<h2 class="titles" transition>Tech Toolbelt</h2>
<p class="parag">The technologies and tooling that i'm familiar with</p>
	<IconPlacer {images}/>
</div>
<style>
	#container{
		width:90%;
		margin-top:2em;
		animation:fade 300ms ease-in;
	}

	@keyframes fade{
		0%{
			transform:translateY(-20%);
			opacity:0;
		}
		100%{
			transform:translateY(0);
			opacity:1;
		}
	}
</style>

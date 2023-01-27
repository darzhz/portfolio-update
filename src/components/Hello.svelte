<script>
import Button from "./Button.svelte";
import DecorT from "./DecorT.svelte";
import Tech from "./Tech.svelte";
import {Download} from "lucide-svelte";
</script>
<div class="main">
<div id="hero">
	<h1 class="titles" id="hi">Hi.</h1>
	<h1 class="titles" id="outline">I'm darsh</h1>
</div>
<div id="image-space">
  <img alt="darsh" src="./prof.png">     </div>
</div>
<p class="parag">I'm a designer, developer and creative personality ready to ship solutions that solve problems to the best of my abilities</p>
<div id="button-field">
	<Button>resumé<Download size="1em"/></Button>
	<Button>Projects</Button>
</div>
<Tech/>
<div id="decor1">
	<DecorT f="slay" m="the" e="web"/>
</div>
<style>
#outline{
  -webkit-text-fill-color: var(--primary);
  -webkit-text-stroke-width: 0.75px;
  -webkit-text-stroke-color: var(--secondary);
  font-size:1.5em;
}
.main{
	display:grid;
	grid-template-columns:1fr 1fr;
}
img{
	height:75%;
	border-radius:50%;
	object-fit:contain;
}
#image-space{
	display:flex;
	justify-content:center;
	align-items:center;
}
#button-field{
	display:flex;
	justify-content:flex-start;
	align-items:center;
	gap:1em;
	margin-top:1em;
}
#decor1{
	position:fixed;
	top:75svh;
	left:60svw;

}
</style>

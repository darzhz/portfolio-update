<script>
export let images
</script>
<div class="panal">
	{#each images as image}
	<img alt={image} src="{image}.svg" style="--order:{images.indexOf(image)+1}">
	{/each}
 </div>
<style>
        .panal > img{
                width:64px;
                height:64px;
                background-size:contain;
		background-repeat:no-repeat;
		background-color:white;
		opacity:0.8;
		padding:0.75rem;
		/*border-radius:50%;
		clip-path: polygon(0% 25%, 0% 75%, 50% 100%, 100% 75%, 100% 25%, 50% 0%);*/

		width: var(--s);
  margin: var(--m);
  height: calc(var(--s) * 1.1547);
  display: inline-block;
  font-size:initial;
  clip-path: polygon(0% 25%, 0% 75%, 50% 100%, 100% 75%, 100% 25%, 50% 0%);
  margin-bottom: calc(var(--m) - var(--s) * 0.2885);

		animation-name: animateIn;
		animation-duration: 800ms;
		animation-delay: calc(var(--order) * 100ms);
 		animation-fill-mode: none;
		animation-timing-function: ease-in-out;
		transition:all 300ms ease-in-out;
        }
	.panal
	{
	display:grid;
	grid-template-columns:repeat(4,1fr);
	grid-template-rows:repeat(4,1fr);
	gap:10px;
  --s: 100px;  /* size  */
  --m: 4px;    /* margin */
  --f: calc(var(--s) * 1.732 + 4 * var(--m) - 1px);

	position:absolute;
	z-index:10;
	}
	.panal > img:hover{
		transform:scale(1.3);
		opacity:1;
	}
	.panal > img::before{
		content: "";
  width: calc(var(--s) / 2 + var(--m));
  float: left;
  height: 120%; 
  shape-outside: repeating-linear-gradient(#0000 0 calc(var(--f) - 3px), #000 0 var(--f));
	}
@keyframes animateIn {
  	0% {
    	opacity: 0;
    	transform: scale(0.2);
  	}

  	100% {
	opacity: 0.8;
	transform:scale(1);
  	}
}
</style>

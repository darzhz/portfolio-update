<script>

</script>
<button><p class="parag" id="btn-parag"><slot></slot></p></button>
<style>
button{
	padding:0.5em 1.25em 0.5em 1.25em;
	min-width:4em;
	border:none;
	border-radius:6em;
	background-color:var(--secondary);
	color:var(--primary);
}
#btn-parag{
	display:flex;
	flex-wrap:nowrap;
	justify-content:center;
	text-align:center;
	vertical-align:baseline;
}
</style>

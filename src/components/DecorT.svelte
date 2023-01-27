<script>
	export let f,m,e;
</script>
	<h3>{f}</h3>
	<p>{m}</p>
	<h3>{e}</h3>
<style>
	h3{
		font-family: 'Anton', sans-serif;
		font-size:5em;
		letter-spacing:0.75rem;
		text-transform:uppercase;
		color:#E4FF72;
		text-shadow:0 0 15px #E4FF72;
		padding:0;
		margin:0;
		line-height:80%;
		text-align:center;
		animation:move 2s infinite;
	}
	h3:nth-child(1) {
		animation-delay: 300ms;
	}
	p{
		font-family: 'Libre Franklin', sans-serif;
		line-height:80%;
		text-align:center;
		font-size:5em;
		letter-spacing:0.50rem;
		text-transform:uppercase;
		color:#E4FF72;
		-webkit-text-fill-color: var(--primary);
		-webkit-text-stroke-width: 0.75px;                      -webkit-text-stroke-color: var(--secondary);
	}
@keyframes move {
	0%, 5%, 95%, 100% {
        left: 0%;
        transform: translate(0, 0);
	}
	45%, 55% {
        left: 20%;
	transform: translate(-20%, 0);
	text-shadow:0 0 17px #E4FF72;
	}
  
	}
</style>

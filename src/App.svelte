<script>
import Hello from "./components/Hello.svelte";
import { Home,Heart,Github,Cog,Download,Linkedin,Twitter,Instagram } from 'lucide-svelte';
</script>
<svelte:head>
<meta name="theme-color" content="#CFFF00" />
</svelte:head>
<div id="body">
	<div id="nav">
	<div class="icon"><Home color="#CFFF00"/></div>
	<div class="icon"><Heart color="#CFFF00"/></div>
	<div class="icon"><Download color="#CFFF00"/></div>
	<div class="icon"><Github color="#CFFF00"/></div>
	<div class="icon"><Instagram color="#CFFF00"/></div>
	<div class="icon"><Linkedin color="#CFFF00"/></div>
	<div class="icon"><Twitter color="#CFFF00"/></div>
	<div class="icon"><Cog color="#CFFF00"/></div>
	</div>
	<div id="content">
	<Hello/>
	</div>
</div>
<style>
.icon{
	min-height:24px;
	min-width:24px;
	padding:0.5em;
	background-color:var(--primary);
	border-radius:50%;
	transition:all 300ms ease-in-out;
	animation:scaleup 250ms ease-in;
	animation-delay:300ms;
	}
#nav{
	animation: movefromleft 250ms cubic-bezier(1,0,0,1);
}

.icon:hover{
	border-top-right-radius:0;
	border-bottom-right-radius:0;
	width:120%;
	scale:1.2;
	}

@keyframes movefromleft{
	0%{
		opacity:0;
		width:0%;
	}
	100%{
		opacity:1;
		width:100%;
	}
}
@keyframes scaleup {
	from{
		transform:scale(0);
		opacity:0;
	}
	to{
		transform:scale(1);
		opacity:1;
	}
}
</style>

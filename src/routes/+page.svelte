<script>
	import Header from './header.svelte';
	import Projects from './projects.svelte'
	import Skills from './skills.svelte'
	import Education from './education.svelte';
	import Testamonials from './testamonials.svelte'
	import './styles.css';
	import Aboutme from './aboutme.svelte';
	import Contact from './contact.svelte';

</script>

<div class="app">
	<Header />
	<Skills />
	<Projects />
	<Testamonials />
	<Education />
	<Aboutme />
	<Contact />
	<slot></slot>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

</style>

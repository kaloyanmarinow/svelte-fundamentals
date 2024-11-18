<script>
	/**
	* Internal dependencies.
	*/
	import Header from '../../../components/Header.svelte';	
	import Footer from '../../../components/Footer.svelte';
	import '../../../global.css';
	import ChildComponent from './ChildComponent.svelte';
</script>

<Header />

<ChildComponent adjective="cool" />

<Footer />
<script>
	import Header from '../components/frontpage/Header.svelte';
	import Footer from '../components/frontpage/Footer.svelte';
	import Section from '../components/frontpage/Section.svelte';
	import About from '../components/frontpage/About.svelte';

	let navItems = [
		{ name: 'Über uns', href: '#about' },
		{ name: 'Projekte', href: '#projects' },
		{ name: 'Spenden', href: '#donations' },
		{ name: 'Partner', href: '#partners' },
		{ name: 'Kontakt', href: '#contact' }
	];
</script>

<Header navigationItems={navItems}></Header>
<Section title="Über uns" id="about" background="white">
	<About/>
</Section>
<Footer></Footer>


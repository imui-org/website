<script>
	import Header from '../components/frontpage/Header.svelte';
	import Footer from '../components/frontpage/Footer.svelte';
	import Section from '../components/frontpage/Section.svelte';
	import About from '../components/frontpage/About.svelte';
	import Projects from '../components/frontpage/Projects.svelte';
	import Donate from '../components/frontpage/Donate.svelte';
	import Partners from '../components/frontpage/Partners.svelte';
	import Contact from '../components/frontpage/Contact.svelte';

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
	<About />
</Section>
<Section title="Projekte" id="projects" background="gray-100">
	<Projects />
</Section>
<Section title="Spenden" id="donate" background="white">
	<Donate />
</Section>
<Section title="Partner und Förderer" id="partners" background="white">
	<Partners />
</Section>
<Section title="Kontakt" id="contact" background="gray-100">
	<Contact />
</Section>
<Footer></Footer>

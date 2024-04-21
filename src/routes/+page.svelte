<script>
	import Header from '../components/frontpage/Header.svelte';
	import Footer from '../components/frontpage/Footer.svelte';

	let navItems = [
		{ name: 'Über uns', href: '#about' },
		{ name: 'Projekte', href: '#projects' },
		{ name: 'Spenden', href: '#donations' },
		{ name: 'Partner', href: '#partners' },
		{ name: 'Contact', href: '#contact' }
	];
</script>

<Header navigationItems={navItems}></Header>
<Footer></Footer>

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.100);
	}
</style>

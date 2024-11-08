<script>
	import '../app.css';
	import '../index.css';
	import Navbar from '../lib/shared/Navbar.svelte';
	import Sidebar from '../lib/shared/Sidebar.svelte';
	import Footer from '../lib/shared/Footer.svelte';
	import {
		faHome,
		faUser,
		faShoppingCart,
		faDoorClosed,
		faBox,
		faShoppingBasket
	} from '@fortawesome/free-solid-svg-icons';
	let { children } = $props();

	const menuItems = [
		{ label: 'Home', icon: faHome, link: '/' },
		{ label: 'Basket', icon: faShoppingBasket, link: '/basket' },
		{ label: 'Cart', icon: faShoppingCart, link: '/cart' },
		{ label: 'Orders', icon: faBox, link: '/orders' },
		{ label: 'Profile', icon: faUser, link: '/profile' },
		{ label: 'Logout', icon: faDoorClosed, link: '/logout' }
	];
</script>

<Navbar />

<Sidebar {menuItems} />
<!-- Main content here -->

{@render children()}

<Footer />

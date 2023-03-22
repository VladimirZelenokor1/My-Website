<script>
	import Header from './Header.svelte';
	import logo from '$lib/images/telegram.png';
	import logo2 from '$lib/images/mail.png';
	import github from '$lib/images/github.svg';
	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>Visit</p>
		<a href="https://t.me/VZ2002"><img src={logo} alt="github">
		<a href="https://github.com/VladimirZelenokor1/My-Website"><img src={github} alt="github">
		<a href="mailto:v.zelenokor@innopolis.university"><img src={logo2} alt="gmail">
	</footer>
</div>

<style>
	img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>

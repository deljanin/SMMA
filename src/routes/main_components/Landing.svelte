<script>
	import { handleAnchorClick } from '$lib/smoothScroll.js';
	import Dots from './dots.svelte';
	import { txt } from '$lib/context.js';
</script>

<div id="landing">
	<h1>{@html $txt.landing.heading1}</h1>
	<h2>{@html $txt.landing.heading2}</h2>
	<a href="#contact" on:click={handleAnchorClick}>
		<button>{$txt.landing.buttonText}</button>
	</a>
	<div class="dots_wrapper">
		<Dots />
	</div>
</div>

<style>
	#landing {
		position: relative;
		width: 100%;
		height: 100vh;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		gap: 0.7em;
	}
	h1,
	h2 {
		z-index: 1;

		color: var(--secondary-color);
		text-align: center;
		cursor: default;
		user-select: none;
	}

	h2 {
		font-size: 2.1em;
		font-family: K2D;
	}
	a {
		z-index: 2;
	}
	button {
		border: none;
		z-index: 2;
		cursor: pointer;
		transform: translateY(13vh);

		font-family: Coolvetica;
		font-size: 2em;
		color: var(--secondary-color);
		border-radius: 100px;
		padding: 0.5em 1.5em;
		background-image: var(--text-gradient);
	}

	.dots_wrapper {
		filter: blur(4px);
		z-index: 0;
		position: absolute;
		top: 8%;
		width: 45%;
	}
</style>

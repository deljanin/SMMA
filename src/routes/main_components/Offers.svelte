<script>
	import { txt } from '$lib/context.js';
	import SilverPlanIcon from '$lib/assets/SilverPlanIcon.svg';
	import GoldPlanIcon from '$lib/assets/GoldPlanIcon.svg';
	import PlatinumPlanIcon from '$lib/assets/PlatinumPlanIcon.svg';
	import { handleAnchorClickCenter } from '$lib/smoothScroll.js';

	const icons = {
		0: SilverPlanIcon,
		1: GoldPlanIcon,
		2: PlatinumPlanIcon
	};
	const links = {
		0: '#silver-plan',
		1: '#gold-plan',
		2: '#platinum-plan'
	};
</script>

<div id="offers">
	<h1>{$txt.whatWeOffer.heading}</h1>
	<div class="cards">
		{#each $txt.whatWeOffer.cards as card, i (card)}
			<div class="group">
				<div class={`vertical-line l${i}`}></div>
				<a href={links[i]} on:click={handleAnchorClickCenter}>
					<div class="card">
						<img src={icons[i]} alt={card.frontText} />
						<span class="powerText frontText">{card.frontText}</span>
						<span class="backText">{card.backText}</span>
					</div>
				</a>
			</div>
		{/each}
	</div>
</div>

<style>
	#offers {
		background-color: var(--primary-color);
		width: 100%;
		height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		gap: 13vh;
	}
	h1 {
		align-self: center;
	}
	.cards {
		display: flex;
		justify-content: space-evenly;
		align-items: center;
	}
	.group {
		position: relative;
	}

	.card {
		padding: 14vh 4vw;
		border-style: solid;
		border-width: 1px;
		border-image: var(--card-border) 30;
		border-radius: 25px;
		text-align: center;
		background-color: var(--transparent-primary);
		backdrop-filter: blur(7px);
		display: flex;
		gap: 4vh;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		cursor: pointer;
	}

	.vertical-line {
		position: absolute;
		top: -22%;
		left: 50%;
		height: 75vh;
		width: 4px;
		background: var(--line-gradient);
	}
	.frontText {
		font-family: Coolvetica;
		font-size: 2.5em;
		display: block;
	}
	.backText {
		display: none;
	}
	img {
		width: 75%;
		height: auto;
	}

	.vertical-line::after {
		content: '';
		display: block;
		position: absolute;
		height: 45px;
		width: 4px;
		border-radius: 25%;
		top: -25%;
		left: 0;
		background: var(--secondary-color);
		opacity: 0;
	}
	.l0::after {
		animation-delay: 2.5s !important;
		animation-timing-function: cubic-bezier(0.4, 0.26, 0, 0.97) !important;
		animation: run 5s forwards infinite;
	}

	.l1::after {
		animation-delay: 2s !important;
		animation-timing-function: cubic-bezier(0.4, 0.26, 0, 0.97) !important;
		animation: run 5s forwards infinite;
	}

	.l2::after {
		animation-delay: 1s !important;
		animation-timing-function: cubic-bezier(0.4, 0.26, 0, 0.97) !important;
		animation: run 5s forwards infinite;
	}
	@keyframes run {
		0% {
			opacity: 0;
			top: -5%;
		}
		20% {
			opacity: 1;
		}
		70% {
			opacity: 1;
		}
		100% {
			opacity: 0;
			top: 90%;
		}
	}
</style>

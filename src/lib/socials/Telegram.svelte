<a href="https://t.me/apexsmma" target="_blank"
	><svg viewBox="0 0 50 50">
		<path
			d="M25.8523 0C12.0721 0 0.888184 11.2 0.888184 25C0.888184 38.8 12.0721 50 25.8523 50C39.6325 50 50.8164 38.8 50.8164 25C50.8164 11.2 39.6325 0 25.8523 0ZM37.4357 17C37.0612 20.95 35.4385 30.55 34.6147 34.975C34.2652 36.85 33.5662 37.475 32.9172 37.55C31.4692 37.675 30.3708 36.6 28.9728 35.675C26.776 34.225 25.5278 33.325 23.4058 31.925C20.9344 30.3 22.5321 29.4 23.955 27.95C24.3295 27.575 30.7203 21.75 30.8451 21.225C30.8625 21.1455 30.8602 21.0629 30.8384 20.9845C30.8167 20.9061 30.7761 20.8342 30.7203 20.775C30.5705 20.65 30.3708 20.7 30.1961 20.725C29.9714 20.775 26.4764 23.1 19.6612 27.7C18.6626 28.375 17.7639 28.725 16.9651 28.7C16.0664 28.675 14.3688 28.2 13.0956 27.775C11.5229 27.275 10.2997 27 10.3995 26.125C10.4494 25.675 11.0736 25.225 12.2469 24.75C19.5364 21.575 24.3794 19.475 26.801 18.475C33.741 15.575 35.1639 15.075 36.1126 15.075C36.3123 15.075 36.7866 15.125 37.0862 15.375C37.3358 15.575 37.4107 15.85 37.4357 16.05C37.4107 16.2 37.4606 16.65 37.4357 17Z"
		/>
		<defs>
			<linearGradient
				id="gradient-telegram"
				x1="0%"
				x2="100%"
				y1="0"
				y2="0"
				gradientUnits="userSpaceOnUse"
			>
				<stop offset="0%" stop-color="var(--secondary-color)" />
				<stop offset="100%" stop-color="var(--secondary-color)" />
			</linearGradient>
		</defs>
	</svg>
</a>

<style>
	svg {
		width: auto;
		height: 35px;
		margin: 0 2px 0 2px;
	}
	path {
		fill: url('#gradient-telegram');
	}
	path ~ defs stop {
		transition: 0.4s;
	}

	a:hover path ~ defs stop:first-child {
		stop-color: #47deb1;
	}
	a:hover path ~ defs stop:last-child {
		stop-color: #fa8cfa;
	}
	@media only screen and (max-width: 700px) {
		svg {
			height: 28px;
		}
	}
	@media only screen and (min-width: 700px) and (max-width: 1139px) {
		svg {
			height: 28px;
		}
	}
</style>

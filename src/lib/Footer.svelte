<footer class="footer">
	<article class="about">
		<p class="description">
			The project is not a lottery and does not guarantee a win. Any contribution and payment is a donation. Making a payment means agreeing to this offer.
			Project ${MAIN_DOMAIN} does not take commission or payment for transactions. The commission of 3% is provided only by the acquiring system when transferring funds. The payment of taxes is the responsibility of the recipient of the funds.
		</p>

		<div class="social">
			<div class="links">
				{#each SOCIAL as item}
					<a href="{item.link}" rel="noopener">
						<img src="/images/{item.name}.svg" alt="{item.name}" width="30" height="30">
					</a>
				{/each}
			</div>

			<span class="info">Idea and implementation by {AUTHOR_FULL}</span>

			<a class="email" href="mailto:{AUTHOR_MAIL}" rel="noopener">{AUTHOR_MAIL}</a>

			<a href="{telegramLink}" target="_blank" class="name">
				<img class="author" src="/images/ravy.png" alt="ravy" />
			</a>
		</div>
	</article>
</footer>

<script>
	import { SOCIAL, AUTHOR_FULL, AUTHOR_MAIL, MAIN_DOMAIN } from '/src/constants'

	export let telegramLink = SOCIAL.find(i => i.name === 'telegram').link
</script>

<style lang="sass">
@import "src/assets/styles/_vars"

.footer
	background: transparent
	width: 100%
	margin-top: 120px

	.about
		display: flex
		flex-direction: column
		justify-content: space-between
		align-items: center
		gap: 120px

		.description
			color: $color_primary
			text-align: center
			padding: 0 20px
			font: 500 14px/20px $main_font_family

		.social
			display: flex
			flex-direction: column
			justify-content: center
			align-items: center
			gap: 20px
			margin-bottom: 50px

			.links
				display: flex
				flex-direction: row
				justify-content: center
				align-items: center
				gap: 40px
				flex-wrap: wrap

			.info
				padding: 0 10px
				text-align: center
				font: 500 14px/1 $main_font_family

			.email
				color: $color_highlight
				text-decoration: none
				font: 600 14px/1 $main_font_family

				&:hover
					text-decoration: underline

			.name
				.author
					max-height: 50px
</style>

<article class="section_two">
	<h2 class="title">Why is this necessary?</h2>
	<p class="description">Each of us does not mind a dollar, it is a small amount. But getting a large sum at once is an event that can change the life of any of us! If 1000 people chip in for $1, then someone will receive $1000 and will be able to pay bills, make a long-awaited purchase, go on vacation or postpone for a great cause. Each of us can put a hand to this and maybe luck will smile on you and it will be you who will receive the community gathering.</p>
</article>

<style lang="sass">
@import "src/assets/styles/_vars"

.section_two
	display: flex
	flex-direction: column
	justify-content: center
	align-items: center
	color: $color_primary
	z-index: 2

	.title
		line-height: 95%
		margin-bottom: 120px
		text-transform: uppercase
		text-align: center
		font: 700 30px/95% $main_font_family

		@media screen and (min-width: 720px)
			font-size: 36px

	.description
		margin-bottom: 120px
		text-align: center
		padding: 0 20px
		font: 500 16px/200% $main_font_family

</style>

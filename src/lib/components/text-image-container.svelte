<script>
	import ContentContainer from '$lib/components/content-container.svelte';

	export let title = 'Who am I?';
	export let text = 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.';
	export let image = '';
</script>

<ContentContainer>
	<h2>{title}</h2>
	<div class='textContainer'>
		<p>
			{text}
		</p>
	</div>
</ContentContainer>
{#if image}
	<div class='background' style='--image: url({image});'>
	</div>
{/if}
<style lang='scss'>
  @import "static/global.scss";

  .background {
    background: var(--image) no-repeat fixed center;
    background-size: cover;
    height: 40vh;

		@supports (-webkit-overflow-scrolling: touch) {
			background-attachment: scroll;
		}
    h2 {
      background: $background;
      position: relative;
      top: 70%;
    }
  }

  .textContainer {
    background-color: $background;
    padding: 40px 50px;

    p {
      color: $color;
      text-align: justify;
    }
  }
</style>
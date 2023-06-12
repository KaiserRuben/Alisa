<script lang='ts'>
	import ContentContainer from './content-container.svelte';
</script>

<ContentContainer>
	<div class='content'>
		<a href='/#'>my work</a>
		<a href='/#'>my bio</a>
	</div>
</ContentContainer>
<style lang='scss'>
  @import "static/global.scss";

  .content {
    z-index: 10;
    background: $background;
    position: absolute;

    //align it on the top left
    top: 7vh;
    right: 0;

    width: max-content;

    //make it scrollable
    overflow-y: scroll;
    overflow-x: hidden;

    //make it look like a modal
    border-radius: 0 0 0 0;
    box-shadow: 0 0 0 0;
    border: 0;

    text-align: right;
    font-size: 1.5rem;
    padding: 1rem 5px 1rem 1rem;

    // slide in from the right
    animation: slide-in 0.2s ease-in-out;
    @keyframes slide-in {
      0% {
        transform: translateX(100%);
      }
      100% {
        transform: translateX(0);
      }
    }

    display: flex;
    flex-direction: column;

  }
</style>
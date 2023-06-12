<script lang='ts'>
	import ContentContainer from '$lib/components/content-container.svelte';
</script>

<svelte:head>
	<title>Alisa - Dance Professionally</title>
</svelte:head>

<!-- Huuuge landing image with my name on it , supposed to have the "Hello there"-effect-->
<section class='helloThere'>
	<ContentContainer>
		<div class='nameContainer'>
			<div class='name'>
				<h1>
					Alisa <br />Mićunović
				</h1>
			</div>
		</div>
	</ContentContainer>

	<!-- Down arrow to show user that there is more content below -->
	<div class='arrowContainer'>
		<svg xmlns='http://www.w3.org/2000/svg' class='icon' viewBox='0 0 512 512'>
			<path fill='none' stroke='#ffffff' stroke-linecap='round' stroke-linejoin='round' stroke-width='48'
						d='M112 184l144 144 144-144' />
		</svg>
	</div>
</section>
<style lang='scss'>
  @import "static/global.scss";

  .nameContainer {
    position: relative;
    width: 100%;
    height: 90vh;
    background-size: cover;
    background: $background url("/assets/Alisa1.webp") no-repeat center;
    overflow: hidden;


    @media screen and (max-width: $mobile) {
      background: $background url("/assets/Alisa1.webp") no-repeat right;
      background-size: cover;
    }
  }

  .name {
    font-weight: bold;
    color: $color; /* Adjust the color as needed to ensure visibility */
    margin: 10vw;

  }


  .arrowContainer {
    text-align: center;
    height: 5vh;
    margin: 3vh 0 2vh 0; //must add up to 5vh, so that it makes 100vh together with the nameContainer and the height of this container
    @media screen and (max-width: $mobile) {
      margin: 2.5vh 0;
    }

    .icon {
      height: 100%;
    }
  }

</style>
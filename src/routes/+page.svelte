<script lang='ts'>
	import ContentContainer from '$lib/components/content-container.svelte';
</script>

<svelte:head>
	<title>Alisa - Dance Professionally</title>
</svelte:head>
<ContentContainer>
	<div class='name'>
		<h1>
			Alisa <br />Mićunović
		</h1>
	</div>
	<img src={`/assets/Alisa1.webp`} alt={`Alisa Dancing 1`} height='100px' width='100px' class='image'>
	<!--	<div class='pictures'>-->
	<!--		{#each [1, 2, 3] as i}-->
	<!--			&lt;!&ndash;			<div style={`&#45;&#45;background-image: url("/assets/Alisa${i}.webp")`} class='img'></div>&ndash;&gt;-->
	<!--			<img src={`/assets/Alisa${i}.webp`} alt={`Alisa Dancing ${i}`} height='100px' width='100px'>-->
	<!--		{/each}-->
	<!--	</div>-->
</ContentContainer>

<style lang='scss'>
  .name {
    margin-top: 15vh;
    position: relative;

  }

  .image {
    width: 100%;
    height: auto;
    margin-top: -15vh;
    z-index: -1;
    position: relative;
  }

  //.pictures {
  //  display: flex;
  //  flex-direction: row;
  //  align-items: center;
  //  max-width: 100%;
  //
  //  img {
  //    object-fit: contain;
  //    height: auto;
  //    width: 25vw;
  //    margin: 0 1vw;
  //  }
  //}
</style>
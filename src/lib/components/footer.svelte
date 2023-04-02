<script lang='ts'>
	import ContentContainer from './content-container.svelte';
</script>
<ContentContainer>
	<div class='content'>
		<a href='/#'>
			Impressum
		</a>
	</div>
</ContentContainer>

<style lang='scss'>
  .content {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    align-items: center;
    height: 100%;
    width: 100%;
    margin-bottom: .8rem;
  }

  span {
    font-size: .8rem;
  }
</style>
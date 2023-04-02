<script>
	import { page } from '$app/stores';
</script>

<div class='container'>
	{#if $page && $page.error && $page.status}
		<h1>{$page.status}: {$page.error.message}</h1>
	{:else}
		<h1>Etwas ist schief gegangen!</h1>
	{/if}
	<a href='/' data-sveltekit-reload><h2>Zurück zur Startseite</h2></a>
</div>

<style lang='sass'>
  @import "../vars"
  .container
    align-items: center
    justify-content: flex-start
    height: 100%
    padding: 5rem 2rem

    h1, h2
      text-align: center

    p
      text-align: center

    img
      height: auto
      max-height: 25vh
      max-width: 40vw
      margin-top: 2rem
</style>

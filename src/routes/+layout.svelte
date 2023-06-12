<script lang='ts'>
	import Header from '$lib/components/header.svelte';
	import Footer from '$lib/components/footer.svelte';
</script>

<div class='page'>
	<!--	<Header />-->
	<div class='content'>
		<slot />
	</div>
	<Footer />
</div>

<style>
    /* Absolute position so that the content can fill inbetween header & footer */
    .page {
        display: flex;
        flex-direction: column;
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        width: 100%;
        min-height: 100%;

        overflow-x: hidden;
    }
</style>

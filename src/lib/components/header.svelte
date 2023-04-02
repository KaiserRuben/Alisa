<script lang='ts'>
	import ContentContainer from './content-container.svelte';
	import Menu from './menu.svelte';

	const toggleMenu = () => {
		menuOpen = !menuOpen;
	};
	let menuOpen = false;
</script>

{#if menuOpen}
	<Menu />
{/if}

<div class='background'>
	<ContentContainer>
		<header>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<svg
				class='hamburger'
				on:click={toggleMenu}
				width='24'
				height='24'
				viewBox='0 0 24 24'
				xmlns='http://www.w3.org/2000/svg'
			>
				<path
					d='M4 6H20M4 12H20M4 18H20'
					stroke-width='1.5'
					stroke-linecap='round'
					stroke-linejoin='round'
				/>
			</svg>
		</header>
	</ContentContainer>
</div>


<style lang='scss'>
  @import '../../vars';

  header {
    display: flex;
    justify-content: flex-end;
    padding-top: 1.5rem;
  }

  .background {
    width: 100%;
    background: transparent;
    position: absolute;
    top: 0;
  }

  .hamburger {
    stroke: $color;
  }
</style>
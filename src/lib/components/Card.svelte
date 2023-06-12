<script lang="ts">
  export let heading: string;
  export let text: string;
  let textShort = "";
  export let image = "";

  $: textShort = text.replace("\n", "<br />").slice(0, 500) + "...";

  let showFullText = false;
</script>

<div class="card" on:click={() => showFullText = true}>
  <div class="card-image" style="background-image: url({image});"></div>
  <div class="card-content">
    <h3 class="card-heading">{heading}</h3>
    <p class="card-text">{@html textShort}</p>
  </div>
</div>

{#if showFullText}
  <div class="showFullText" on:click={() => showFullText = false}>
    <p>
      {@html text.replace('\n', '<br /><br />')}
    </p>
  </div>
{/if}

<style lang="scss">
  @import "static/global.scss";

  .card {
    width: 400px;
    max-width: 90vw;
    margin: 20px;
    border-radius: 5px;
    box-shadow: 0 0 5px 5px rgba($color, 0.5);;
    overflow: hidden;
  }

  .card-image {
    background-size: cover;
    height: 200px;
  }

  .card-content {
    padding: 0 20px 20px 20px;
    height: 350px;
    cursor: pointer;

    p {
      text-align: justify;
    }
  }

  .card-heading {
    margin-bottom: 10px;
  }

  .showFullText {
    position: fixed;
    top: 0;
    left: 0;
    width: 80vw;
    height: 100vh;
    background: rgba(0, 0, 0, 0.5);
    z-index: 100;
    backdrop-filter: blur(8px) saturate(10%);
    // safari
    -webkit-backdrop-filter: blur(8px) saturate(10%);

    padding: 0 10vw;

    display: flex;
    align-items: center;
    justify-content: center;

    text-align: justify;

    cursor: pointer;

    @media screen and (max-width: $mobile) {
      position: absolute;
      p {
        font-size: .7rem;
        line-height: 1.25;
        font-weight: 400;
      }
    }
  }
</style>
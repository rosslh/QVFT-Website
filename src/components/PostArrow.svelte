<script>
  export let left;
  export let style;
</script>

<style>
  .arrowRight {
    z-index: 6;
    width: 0;
    height: 0;
    border-top: 16px solid transparent;
    border-bottom: 16px solid transparent;
    position: absolute;
    top: 50%;
    transform: translate(50%, -50%);
    right: 1.7rem;
    border-left: 16px solid white;
  }

  .arrowRightBorder {
    z-index: 2;
    width: 0;
    height: 0;
    border-top: 18px solid transparent;
    border-bottom: 18px solid transparent;
    position: absolute;
    top: 50%;
    transform: translate(50%, -50%);
    right: 1.7rem;
    border-left: 18px solid #ddd;
  }

  .arrowLeft {
    z-index: 6;
    width: 0;
    height: 0;
    border-top: 16px solid transparent;
    border-bottom: 16px solid transparent;
    position: absolute;
    top: 50%;
    transform: translate(-50%, -50%);
    left: 1.7rem;
    border-right: 16px solid white;
  }

  .arrowLeftBorder {
    z-index: 2;
    width: 0;
    height: 0;
    border-top: 18px solid transparent;
    border-bottom: 18px solid transparent;
    position: absolute;
    top: 50%;
    transform: translate(-50%, -50%);
    left: 1.7rem;
    border-right: 18px solid #ddd;
  }
</style>

{#if left}
  <div aria-hidden="true" {style} class="arrowLeft" />
  <div aria-hidden="true" {style} class="arrowLeftBorder" />
{:else}
  <div aria-hidden="true" {style} class="arrowRight" />
  <div aria-hidden="true" {style} class="arrowRightBorder" />
{/if}

<script lang="ts">
    export let progress = 0,
        width = '100%',
        indeterminate = false
</script>

<style lang="scss">
  .progressContainer {
    position: relative;
    height: 6px;
    border-radius: 50px;
    overflow: hidden;
    transition: all 0.3s ease;
  }

  .progressBar {
    position: absolute;
    height: 4px;
    top: 1px;
    width: 100%;
    background-color: #e0e0e0;
    border-radius: 50px;
  }

  .progressIndicator {
    position: absolute;
    top: -1px;
    left: 0;
    height: 6px;
    background-color: var(--mt-primary);
    border-radius: 5px;
    transition: all 0.3s ease;
  }

  .ind-1 {
    animation: ind-1 3s ease-in infinite;
  }

  .ind-2 {
    animation: ind-2 3s ease-out infinite;
  }

  @keyframes ind-1 {
    0% {
      left: 0;
      width: 0;
    }

    65% {
      left: 100%;
      width: 150%;
    }

    100% {
      left: 100%;
      width: 0;
    }
  }

  @keyframes ind-2 {
    0% {
      left: -150%;
      width: 150%;
    }

    55% {
      left: -150%;
      width: 150%;
    }

    90% {
      left: 100%;
      width: 9%;
    }

    100% {
      left: 100%;
      width: 9%;
    }
  }
</style>

<div class="progressContainer" style="width: {width};">
    <div class="progressBar">
        {#if indeterminate}
            <div class="progressIndicator ind-1"></div>
            <div class="progressIndicator ind-2"></div>
        {:else}
            <div class="progressIndicator" style="width: {progress * 100}%"></div>
        {/if}
    </div>
</div>

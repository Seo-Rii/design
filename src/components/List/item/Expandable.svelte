<script lang="ts">
    let show, container, originalHeight = 0;

    function toggle() {
        originalHeight = container.clientHeight;
        show = !show;
    }
</script>

<style lang="scss">
  .list {
    overflow: hidden;
    height: 0;
    transition: all .2s;

    &.show {
      height: var(--original-height);
    }
  }
</style>

<div class="container">
    <div on:click={toggle}>
        <slot name="meta" expanded={show}/>
    </div>
    <div class:show class="list" style="--original-height: {originalHeight}px">
        <div bind:this={container}>
            <slot/>
        </div>
    </div>
</div>
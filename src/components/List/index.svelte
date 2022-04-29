<script lang="ts">
    import TwoLine from "./item/TwoLine.svelte";
</script>

<style lang="scss">
  .list {
    border-radius: 10px;
    position: relative;
    z-index: 1;
    overflow: hidden;

    &:before {
      content: " ";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      opacity: .8;
      z-index: -1;
      background-color: #ffffff;
    }
  }
</style>

<div class="list">
    <div class="container">
        <slot/>
    </div>
</div>
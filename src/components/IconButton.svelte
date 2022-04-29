<script lang="ts">
    import Ripple from "./Ripple.svelte";

    export let icon,
        size: ('small' | 'medium' | 'large') = 'medium';
</script>

<style lang="scss">
  $small-padding: 12px;
  $medium-padding: 16px;
  $large-padding: 20px;

  button {
    border: 0;
    border-radius: 50%;
    cursor: pointer;
    display: inline-block;
    line-height: 1;
    background: transparent;
    z-index: 2;
    position: relative;
    overflow: hidden;

    -webkit-tap-highlight-color: transparent;
    outline: none;
    -ms-touch-action: manipulation;
    touch-action: manipulation;

    &.small {
      font-size: 14px;
      padding: $small-padding;
    }

    &.medium {
      font-size: 20px;
      padding: $medium-padding;
    }

    &.large {
      font-size: 28px;
      padding: $large-padding;
    }
  }
</style>

<button type='button' class="icon {size}">
    {icon}
    <Ripple zIndex={2} center primary={false}/>
</button>
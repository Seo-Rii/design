<script lang="ts">
    import Ripple from "../Ripple.svelte";

    export let active = false, icon = '', indicator = active, ripple = true;
</script>

<style lang="scss">
  .footerItem {
    width: 60px;
    height: 60px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
    color: #8e8e8e;
    cursor: pointer;

    -webkit-tap-highlight-color: transparent;
    outline: none;
    -ms-touch-action: manipulation;
    touch-action: manipulation;

    &.active {
      color: #000000;
    }

    span {
      font-size: 32px !important;
    }

    * {
      margin: 1px;
    }

    .indicator {
      width: 5px;
      height: 5px;
      border-radius: 50%;
      background: #000000;
    }
  }
</style>


<div class:active class="footerItem icon">
    <span>{icon}</span>
    {#if indicator}
        <div class="indicator"/>
    {/if}
    {#if ripple}
        <Ripple center primary={false} bound={2}/>
    {/if}
</div>
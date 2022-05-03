<script lang="ts">
    import Ripple from "../../Ripple.svelte";

    export let title: '',
        subtitle: '';
</script>

<style lang="scss">
  .container {
    display: flex;
    align-items: center;
    padding: 10px;
    position: relative;
    overflow: hidden;
    cursor: pointer;

    -webkit-tap-highlight-color: transparent;
    outline: none;
    -ms-touch-action: manipulation;
    touch-action: manipulation;

    .head {
      height: 50px;
      width: 50px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 10px;
    }

    .body {
      display: flex;
      flex-direction: column;
    }

    .suffix {
      margin-left: auto;
    }

    h1 {
      font-size: 24px;
      margin: 2px;
      font-weight: 700;
    }

    h2 {
      font-size: 16px;
      margin: 2px;
      font-weight: 500;
    }
  }
</style>

<div>
    <div class="container">
        {#if $$slots.prefix}
            <div class="prefix">
                <slot name="prefix"></slot>
            </div>
        {/if}
        <div class="body">
            <h1>{title}</h1>
            <h2>{subtitle}</h2>
        </div>
        {#if $$slots.suffix}
            <div class="suffix">
                <slot name="suffix"></slot>
            </div>
        {/if}
        <Ripple primary={false}/>
    </div>
</div>
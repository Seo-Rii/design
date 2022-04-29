<script lang="ts">
    import Ripple from "../../Ripple.svelte";

    export let meta: any,
        title: '';
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

    h1 {
      font-size: 24px;
      margin: 2px;
      font-weight: 700;
    }
  }
</style>

<div>
    <div class="container">
        {#if meta}
            <div class="head">{meta}</div>
        {/if}
        <div class="body">
            <h1>{title}</h1>
        </div>
        <Ripple primary={false}/>
    </div>
</div>
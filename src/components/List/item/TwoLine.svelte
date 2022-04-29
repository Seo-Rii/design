<script lang="ts">
    import Ripple from "../../Ripple.svelte";

    export let meta: any,
        title: '',
        subtitle: '';
</script>

<style lang="scss">
  .container {
    display: flex;
    align-items: center;

    .head {
      height: 50px;
      width: 50px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-right: 10px;
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
        {#if meta}
            <div class="head">{meta}</div>
        {/if}
        <div>
            <h1>{title}</h1>
            <h2>{subtitle}</h2>
        </div>
        <Ripple/>
    </div>
</div>
<script lang="ts">
    import IconButton from "../IconButton.svelte";

    export let subtitle = '', back = false;
    let scrollY;
</script>

<style lang="scss">
  header {
    transition: all 0.3s ease-in-out;
    position: fixed;
    width: 100%;
    height: 62px;
    z-index: 5;
    border-bottom: 0px solid #ffffff00;
    top: -1px;
    left: 0;

    .container {
      display: flex;
      align-items: center;
    }

    .titleContainer {
      position: relative;
      width: 100px;
      height: 32px;
    }

    .title, .subtitle {
      position: absolute;
      left: 0;
      transition: all 0.3s ease-in-out;
    }

    .title {
      opacity: 1;
      margin-left: 20px !important;
      margin-right: -20px !important;
    }

    .subtitle {
      opacity: 0;
      margin-left: 40px !important;
      margin-right: -40px !important;
    }

    &.raised {
      box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
      //backdrop-filter: blur(5px);
      //border-bottom: 1px solid #e6e6e6;

      .dynamic {
        .title {
          opacity: 0;
          margin-left: 40px !important;
          margin-right: -40px !important;
        }

        .subtitle {
          opacity: 1;
          margin-left: 20px !important;
          margin-right: -20px !important;
        }
      }
    }

    &:before {
      content: " ";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      opacity: 1;
      z-index: -1;
      background-color: var(--mt-surface);
    }

    .wrapper {
      font-family: 'Nunito Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 10px;
      height: 62px;
    }

    h1 {
      font-weight: 900;
      font-size: 20px !important;
      line-height: 1;
      margin: 6px 0 6px 10px;
      display: inline-block;
      vertical-align: top;
    }
  }

  .marginFix {
    height: 62px;
  }
</style>

<svelte:window bind:scrollY/>
<header class:raised={scrollY>0}>
    <div class="wrapper" class:dynamic={subtitle}>
        <div class="container">
            {#if back}
                <IconButton icon={'arrow_back'}/>
            {/if}
            <div class="titleContainer">
                <h1 class="title">MealCamp</h1>
                {#if subtitle}
                    <h1 class="subtitle">{subtitle}</h1>
                {/if}
            </div>
        </div>
        <div>
            <IconButton icon={'notifications'}/>
        </div>
    </div>
</header>
<div class="marginFix"/>
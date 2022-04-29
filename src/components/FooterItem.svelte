<script lang="ts">
    export let text = '',
        icon = '',
        active = false,
        ripple = true,
        indicator = active;
</script>

<style lang="scss">
  div {
    width: 60px;
    height: 60px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
    color: #8e8e8e;

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

<div class:active>
    <span style="font-size:16px;">{icon}</span>
    {indicator && <div class="indicator"/>}
    {ripple && <Ripple center/>}
</div>
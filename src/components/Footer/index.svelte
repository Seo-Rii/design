<style lang="scss">
  footer {
    transition: all 0.3s ease-in-out;
    position: fixed;
    width: 100%;
    height: 62px;
    z-index: 5;
    bottom: -1px;
    left: 0;
    background: #ffffff;
    border-radius: 15px 15px 0 0;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
    user-select: none;
    overflow: hidden;
    padding-bottom: 10px;

    .wrapper {
      display: flex;
      align-items: center;
      justify-content: space-around;
      padding: 0 10px;
      height: 62px;
    }
  }

  .marginFix {
    height: 62px;
  }
</style>

<div class="marginFix"/>
<footer>
    <div class="wrapper">
        <slot/>
    </div>
</footer>
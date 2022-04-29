<style lang="scss">
  div {
    width: 100%;
    height: 100%;
    padding: 10px;
    margin: 0;
    background: var(--mt-surface);

    & :global(*) {
      font-family: 'Noto Sans KR', sans-serif;
    }

    & :global(h1) {
      font-size: 36px;
      font-weight: 700;
      margin: 6px 0 6px 10px;
      display: inline-block;
    }

    & :global(h2) {
      font-size: 24px;
      font-weight: 700;
      margin: 6px 0 6px 10px;
      display: inline-block;
    }

    & :global(main) {
      padding: 20px;
    }
  }
</style>

<div>
    <slot/>
</div>
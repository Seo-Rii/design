<script lang="ts">
    import OneLine from "../item/OneLine.svelte";
    import TwoLine from "../item/TwoLine.svelte";
    import IconButton from "../../IconButton.svelte";
</script>

<style lang="scss">
  .expandMenu {
    transition: all 0.3s ease;

    &.expanded {
      transform: rotate(180deg);
    }
  }
</style>

<TwoLine title="소고기덮밥" subtitle="풀빛마루, 오늘">
    <IconButton slot="prefix" icon="restaurant"/>
</TwoLine>
<TwoLine title="치즈돈까스" subtitle="오늘도든든, 오늘">
    <IconButton slot="prefix" icon="restaurant"/>
</TwoLine>

<OneLine title="더 보기">
    <IconButton slot="prefix" icon="more_horiz" ripple={false}/>
</OneLine>



<script lang="ts">
    import TwoLine from "../item/TwoLine.svelte";
    import IconButton from "../../IconButton.svelte";
    import Expandable from "../item/Expandable.svelte";
</script>

<style lang="scss">
  .expandMenu {
    transition: all 0.3s ease;

    &.expanded {
      transform: rotate(180deg);
    }
  }
</style>

<TwoLine title="메뉴" subtitle="6000원">
    <IconButton slot="prefix" icon="restaurant"/>
</TwoLine>

<TwoLine title="메뉴" subtitle="6000원">
    <IconButton slot="prefix" icon="restaurant"/>
</TwoLine>

<TwoLine title="메뉴" subtitle="6000원">
    <IconButton slot="prefix" icon="restaurant"/>
</TwoLine>



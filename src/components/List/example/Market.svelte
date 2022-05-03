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

<TwoLine title="풀빛마루" subtitle="3분">
    <IconButton slot="prefix" icon="restaurant"/>
</TwoLine>

<Expandable>
    <TwoLine title="카이마루" subtitle="3개 음식점" slot="meta" let:expanded>
        <IconButton slot="prefix" icon="checklist"/>
        <div slot="suffix" class="expandMenu" class:expanded>
            <IconButton icon="expand_more" ripple={false}/>
        </div>
    </TwoLine>
    <TwoLine title="오늘도든든" subtitle="3분">
        <IconButton slot="prefix" icon="rice_bowl"/>
    </TwoLine>
    <TwoLine title="롯데리아" subtitle="3분">
        <IconButton slot="prefix" icon="lunch_dining"/>
    </TwoLine>
</Expandable>



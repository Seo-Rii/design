<script lang="ts">
    import OneLine from "../item/OneLine.svelte";
    import IconButton from "../../IconButton.svelte";
    import Badge from "../../Badge.svelte";
</script>

<style lang="scss">
  .expandMenu {
    transition: all 0.3s ease;

    &.expanded {
      transform: rotate(180deg);
    }
  }
</style>

<OneLine title="카드">
    <IconButton slot="prefix" icon="payment" ripple={false}/>
    <Badge slot="suffix" label="최근에 쓴"/>
</OneLine>
<OneLine title="PAYCO">
    <IconButton slot="prefix" icon="toll" ripple={false}/>
</OneLine>
<OneLine title="토스">
    <IconButton slot="prefix" icon="toll" ripple={false}/>
</OneLine>
<OneLine title="네이버페이">
    <IconButton slot="prefix" icon="toll" ripple={false}/>
</OneLine>
<OneLine title="카카오페이">
    <IconButton slot="prefix" icon="toll" ripple={false}/>
</OneLine>
<OneLine title="메뉴 더 고르기">
    <IconButton slot="prefix" icon="close" ripple={false}/>
</OneLine>



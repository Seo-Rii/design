<script lang="ts">
    import FooterItem from '../item.svelte';
    import Progress from "../../Progress.svelte";
</script>

<FooterItem icon='shopping_cart' ripple={false} active indicator={false}/>
<div style="width:20%;">
    <Progress progress={1} color='var(--mt-on-surface)'/>
</div>
<FooterItem icon='payments' ripple={false} active indicator={false}/>
<div style="width:20%;">
    <Progress progress={0.5} color='var(--mt-on-surface)'/>
</div>
<FooterItem icon='takeout_dining' ripple={false}/>
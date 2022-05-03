<script lang="ts">
    import FooterItem from "../item.svelte";

    export let active = '홈'
</script>

<FooterItem icon='notifications' text='알림' active={active==='알림'}/>
<FooterItem icon='home' text='홈' active={active==='홈'}/>
<FooterItem icon='account_circle' text='계정' active={active==='계정'}/>
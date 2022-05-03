<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import {viewportConfig} from '../util/config'
    import MyPage from "../../pages/MyPage.svelte";
</script>

<Meta title="Page/MyPage" component={MyPage} parameters={{
        layout: 'fullscreen',
        ...viewportConfig(true),
    }}
/>

<Template let:args>
    <MyPage/>
</Template>

<Story name="MyPage"/>
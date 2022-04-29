<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import {viewportConfig} from '../util/config'
    import Shop from "../../pages/Shop.svelte";
</script>

<Meta title="Page/Shop" component={Shop} parameters={{
        layout: 'fullscreen',
        ...viewportConfig(true),
    }}
/>

<Template let:args>
    <Shop/>
</Template>

<Story name="Shop"/>
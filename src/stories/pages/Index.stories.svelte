<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import {viewportConfig} from '../util/config'
    import Index from "../../pages/Index.svelte";
</script>

<Meta title="Page/Index" component={Index} parameters={{
        layout: 'fullscreen',
        ...viewportConfig(true),
    }}
/>

<Template let:args>
    <Index/>
</Template>

<Story name="Index"/>
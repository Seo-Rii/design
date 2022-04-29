<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import Header from "../../components/Header/index.svelte";
    import Container from "../../components/Container.svelte";
    import LoremIpsum from "../util/LoremIpsum.svelte";
</script>

<Meta
        title="Components/Header"
        component={Header}
        argTypes={{
    back: { control: "boolean" },
    subtitle: { control: "text" },
  }}
/>

<Template let:args>
    <Container>
        <Header {...args}/>
        <LoremIpsum/>
    </Container>
</Template>

<Story name="Main" args={{
    back:false,
    subtitle:'',
  }}
/>

<Story name="Sub" args={{
    back:true,
    subtitle:'Menu',
  }}
/>

<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import List from "../../components/List/index.svelte";
    import Container from "../../components/Container.svelte";
</script>

<Meta title="Components/List" component={List} argTypes={{
    progress: { control: { type: 'range', min: 0, max: 1, step: 0.01 } },
    indeterminate: { control: "boolean" },
  }}
/>

<Template let:args>
    <Container>
        <List/>
    </Container>
</Template>

<Story name="One Line" args='t1'/>

<Story name="Two Line" args='t2'/>
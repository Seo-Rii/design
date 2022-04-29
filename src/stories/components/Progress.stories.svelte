<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import Progress from "../../components/Progress.svelte";
    import Container from "../../components/Container.svelte";
</script>

<Meta title="Components/Progress" component={Progress} argTypes={{
    progress: { control: { type: 'range', min: 0, max: 1, step: 0.01 } },
    indeterminate: { control: "boolean" },
  }}
/>

<Template let:args>
    <Container>
        <Progress {...args}/>
    </Container>
</Template>

<Story name="Determinate" args={{
    indeterminate: false,
    progress: 0.5,
  }}
/>

<Story name="Indeterminate" args={{
    indeterminate: true,
  }}
/>
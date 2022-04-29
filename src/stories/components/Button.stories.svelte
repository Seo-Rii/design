<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import Button from "../../components/Button.svelte";
    import Container from "../../components/Container.svelte";
</script>

<Meta
        title="Components/Button"
        component={Button}
        argTypes={{
    label: { control: "text" },
    primary: { control: "boolean" },
    raised: { control: "boolean" },
    size: {
      control: { type: 'select' },
      options: ['small', 'medium', 'large'],
    },
  }}
/>

<Template let:args>
    <Container>
        <Button {...args} on:click={args.onClick}>{args.label}</Button>
    </Container>
</Template>

<Story name="Primary" args={{
    label: "Button",
    primary: true,
  }}
/>

<Story name="Secondary" args={{
    label: "Button",
  }}
/>

<Story name="Large" args={{
    label: "Button",
    size: "large",
  }}
/>

<Story name="Small" args={{
    label: "Button",
    size: "small",
  }}
/>

<Story name="Raised" args={{
    label: "Button",
    raised: true,
    primary: true,
  }}
/>

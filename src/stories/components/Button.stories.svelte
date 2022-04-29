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

<Story
        name="Primary"
        args={{
    primary: true,
    label: "Button",
  }}
/>

<Story
        name="Secondary"
        args={{
    label: "Button",
  }}
/>
<Story
        name="Large"
        args={{
    size: "large",
    label: "Button",
  }}
/>

<Story
        name="Small"
        args={{
    size: "small",
    label: "Button",
  }}
/>

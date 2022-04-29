<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import IconButton from "../../components/IconButton.svelte";
    import Container from "../../components/Container.svelte";
</script>

<Meta
        title="Components/IconButton"
        component={IconButton}
        argTypes={{
    icon: { control: "text" },
    size: {
      control: { type: 'select' },
      options: ['small', 'medium', 'large'],
    },
  }}
/>

<Template let:args>
    <Container>
        <IconButton {...args} on:click={args.onClick}/>
    </Container>
</Template>

<Story
        name="IconButton"
        args={{
    icon:'add'
  }}
/>
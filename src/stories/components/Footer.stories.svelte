<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import Footer from "../../components/Footer/index.svelte";
    import Container from "../../components/Container.svelte";

    import LoremIpsum from "../util/LoremIpsum.svelte";
    import FooterItem_main from '../../components/Footer/item/Main.svelte'
    import FooterItem_buy from '../../components/Footer/item/Buy.svelte'
</script>

<Meta
        title="Components/Footer"
        component={Footer}
        argTypes={{
    page: {
      control: { type: 'select' },
      options: ['Main', 'Buy'],
    },
  }}
/>

<Template let:args>
    <Container>
        <LoremIpsum/>
        {#if args.page === 'Main'}
            <Footer>
                <FooterItem_main/>
            </Footer>
        {/if}
        {#if args.page === 'Buy'}
            <Footer>
                <FooterItem_buy/>
            </Footer>
        {/if}
    </Container>
</Template>

<Story name="Main" args={{page:'Main'}}/>
<Story name="Buy" args={{page:'Buy'}}/>

<script>
    import '../../style/theme.scss'
    import {Meta, Template, Story} from "@storybook/addon-svelte-csf";
    import List from "../../components/List/index.svelte";
    import Container from "../../components/Container.svelte";

    import OneLine from "../../components/List/item/OneLine.svelte";
    import TwoLine from "../../components/List/item/TwoLine.svelte";
    import Test from "../../components/List/example/Market.svelte";
</script>

<Meta title="Components/List" component={List} argTypes={{
    type: {
      control: { type: 'select' },
      options: ['One Line', 'Two Line', 'Test'],
    },
  }}
/>

<Template let:args>
    <Container>
        <List>
            {#if args.type === 'One Line'}
                <OneLine title="풀빛마루"/>
            {/if}
            {#if args.type === 'Two Line'}
                <TwoLine title="풀빛마루" subtitle="3분"/>
            {/if}
            {#if args.type === 'Test'}
                <Test/>
            {/if}
        </List>
    </Container>
</Template>

<Story name="One Line" args={{type:'One Line'}}/>
<Story name="Two Line" args={{type:'Two Line'}}/>
<Story name="Test" args={{type:'Test'}}/>
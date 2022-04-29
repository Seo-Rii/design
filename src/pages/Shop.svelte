<script lang="ts">
    import Container from "../components/Container.svelte";
    import Header from "../components/Header/index.svelte";
    import List from "../components/List/index.svelte";
    import ListBody from "../components/List/example/Market.svelte";
    import Footer from "../components/Footer/index.svelte";
    import FooterBody from "../components/Footer/item/Buy.svelte";
</script>

<Container>
    <Header subtitle="풀빛마루" back/>
    <main>
        <h2>풀빛마루</h2>
        <h2 style="font-weight: 400;margin-left: 0;">에서</h2>
        <br/>
        <h1>뭐를 먹을까요?</h1>
        <div style="height: 20px;"/>
        <List>
            <ListBody/>
        </List>
    </main>
    <Footer>
        <FooterBody/>
    </Footer>
</Container>
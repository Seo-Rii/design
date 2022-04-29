<script lang="ts">
    import Container from "../components/Container.svelte";
    import Header from "../components/Header/index.svelte";
    import List from "../components/List/index.svelte";
    import ListBody from "../components/List/example/Market.svelte";
    import Footer from "../components/Footer/index.svelte";
    import FooterBody from "../components/Footer/item/Main.svelte";
</script>

<Container>
    <Header/>
    <main>
        <h1>점심은</h1>
        <br/>
        <h1>어디서 먹을까요?</h1>
        <div style="height: 20px;"/>
        <List>
            <ListBody/>
        </List>
    </main>
    <Footer>
        <FooterBody/>
    </Footer>
</Container>
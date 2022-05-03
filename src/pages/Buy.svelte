<script lang="ts">
    import Container from "../components/Container.svelte";
    import Header from "../components/Header/index.svelte";
    import List from "../components/List/index.svelte";
    import ListBody from "../components/List/example/Buy.svelte";
    import Footer from "../components/Footer/index.svelte";
    import FooterBody from "../components/Footer/item/Buy.svelte";
</script>

<Container>
    <Header/>
    <main>
        <h2>치즈돈까스</h2>
        <h2 style="font-weight: 400;margin-left: 0;">는</h2>
        <br/>
        <h2>3000원</h2>
        <h2 style="font-weight: 400;margin-left: 0;">이에요.</h2>
        <br/>
        <h1>어떻게 결제할까요?</h1>
        <div style="height: 20px;"/>
        <List>
            <ListBody/>
        </List>
    </main>
    <Footer>
        <FooterBody/>
    </Footer>
</Container>
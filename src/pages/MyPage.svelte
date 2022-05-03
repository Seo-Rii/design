<script lang="ts">
    import Container from "../components/Container.svelte";
    import Header from "../components/Header/index.svelte";
    import List from "../components/List/index.svelte";
    import ListBody1 from "../components/List/example/History.svelte";
    import Footer from "../components/Footer/index.svelte";
    import FooterBody from "../components/Footer/item/Main.svelte";
    import Margin from "../components/Margin.svelte";
</script>

<Container>
    <Header/>
    <main>
        <h2>이서현</h2>
        <h2 style="font-weight: 400;margin-left: 0;">님,</h2>
        <br/>
        <h1>점심은 맛있었어요?</h1>
        <Margin size="20"/>

        <h2>최근 메뉴</h2>
        <Margin size="5"/>
        <List>
            <ListBody1/>
        </List>
        <Margin size="15"/>

        <h2>최근 메뉴</h2>
        <Margin size="5"/>
        <List>
            <ListBody1/>
        </List>
        <Margin size="15"/>
    </main>
    <Footer>
        <FooterBody active="계정"/>
    </Footer>
</Container>
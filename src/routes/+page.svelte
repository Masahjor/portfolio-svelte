<script lang="ts">
    import '../app.css';
    import Header from './Header.svelte';
    import Main from './Main.svelte';
    import Footer from './Footer.svelte';
    let { children } = $props();
</script>

<main>
    <Header />
    <Main />
    <Footer />
</main>

<style>
    /* Remove the background animation from here */
    :global(main) {
        height: auto; /* Adjust height as needed */
    }
</style>
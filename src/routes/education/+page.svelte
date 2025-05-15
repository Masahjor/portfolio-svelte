<!-- Script -->
<script lang="ts">

    import Header from '../Header.svelte';
    import Footer from '../Footer.svelte';
    import Main from './Main.svelte';
    let { children } = $props();
</script>

<!-- HTML -->
<main>
    <Header />

    <Main />

    <Footer />
</main>


<!-- CSS -->
<style>

</style>


<!-- End of code snippet -->
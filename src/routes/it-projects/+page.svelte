<!-- Script -->
<script lang="ts">

    import Header from '../Header.svelte';
    import Footer from '../Footer.svelte';
    let { children } = $props();
</script>

<!-- HTML -->
<main>
    <Header />
    


    <Footer />
</main>


<!-- CSS -->
<style>
    main {
        background-color: black;
        min-height: 100vh;
    }

</style>


<!-- End of code snippet -->
<!-- Script -->
<script lang="ts">
    import '../app.css';
    import Header from './Header.svelte';
    import Footer from './Footer.svelte';
    let { children } = $props();
</script>

<!-- HTML -->
<main>
    <Header />
    
    <div class="test-container">
        <h1>Welcome to SvelteKit</h1>
        <p>To get started, edit <code>src/routes/+page.svelte</code> and save to reload.</p>
        <p><a href="https://kit.svelte.dev/docs/introduction">Documentation</a></p>
        <p><a href="https://svelte.dev/repl">REPL</a></p>
    </div>


    <Footer />
</main>


<!-- CSS -->
<style>
    main {
        background-color: black;
        min-height: 100vh;
    }

    .test-container {
        background-color: #333;
        padding: 1em;
        max-width: 600px;
        margin: auto;
    }
    h1 {
        color: #ff3e00;
        font-size: xx-large;
        padding-bottom: 15px;
    }
    p {
        color: #f4f4f4;
    }
    a {
        color: #ff3e00;
        text-decoration: none;
    }
    a:hover {
        text-decoration: underline;
    }
    code {
        background: #ff3e00;
        padding: 0.2em 0.4em;
        border-radius: 3px;
    }
    @media (prefers-color-scheme: dark) {
        .test-container {
            background: #333;
            color: #fff;
        }

    }
</style>


<!-- End of code snippet -->
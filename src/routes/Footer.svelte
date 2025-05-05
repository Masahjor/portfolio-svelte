<!-- script -->
<script lang="ts">
    // Add any necessary imports for icons if using a library like FontAwesome
</script>

<!-- HTML -->
<main>
    <h2>Socials</h2>
    <div class="social-icons">
        <a class="SoMe-icon" href="https://www.youtube.com/@masahjor" target="_blank" rel="noopener noreferrer">
            <img src="youtube-logo.png" alt="Youtube" />
        </a>
        <a class="SoMe-icon" href="https://bsky.app/profile/masahjor.bsky.social" target="_blank" rel="noopener noreferrer">
            <img src="bsky-logo.png" alt="Bluesky" />
        </a>
        <a class="SoMe-icon" href="https://github.com/Masahjor" target="_blank" rel="noopener noreferrer">
            <img src="github-logo.png" alt="Github" />
        </a>
        <a class="SoMe-icon" href="https://cara.app/masahjor" target="_blank" rel="noopener noreferrer">
            <img src="cara-logo.png" alt="Cara" />
        </a>
    </div>
    <p class="footer-note">
        Build with <a href="https://svelte.dev/" target="_blank" rel="noopener noreferrer" class="sveltekit">Sveltekit</a> & <a href="https://tailwindcss.com/" target="_blank" rel="noopener noreferrer" class="tailwind">Tailwind</a>
    </p>
</main>

<!-- CSS -->
<style>
    @font-face {
        font-family: 'Nexa-Heavy.ttf';
        src: url('Nexa-Heavy.ttf') format('truetype');
    }

    main {
        font-family: 'Nexa-Heavy.ttf', sans-serif;
        background-color: lightgray;
        padding: 1em;
        height: auto;
        margin: auto;
        width: 100%;
        position: fixed;
        left: 0;
        bottom: 0;
        text-align: center;
    }

    h2 {
        margin: 0.5em 0;
        font-size: 1.5em;
    }

    .social-icons {
        display: flex;
        justify-content: center;
        gap: 1em;
        margin: 1em 0;
    }

    .social-icons img {
        width: 48px;
        height: 48px;
    }

    .footer-note {
        position: absolute;
        right: 1em;
        bottom: 1em;
        font-size: 0.9em;
    }

    .sveltekit {
        color: #ff3e00;
    }

    .tailwind {
        color: #3f48cc;
    }
    
    .SoMe-icon {
        transition: transform .2s;
    }
    .SoMe-icon:hover {
        transform: scale(1.5)
        ;
    }
</style>
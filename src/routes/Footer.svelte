<!-- script -->
<script lang="ts">
    // Add any necessary imports for icons if using a library like FontAwesome
</script>

<!-- HTML -->
<div class="footer">
    <!-- The pain I endure to create a fancy background kills me -->
    <h2>Socials</h2>
    <div class="social-icons">
        <a class="SoMe-icon youtube" href="https://www.youtube.com/@masahjor" target="_blank" rel="noopener noreferrer">
            <img src="youtube-logo.png" alt="Youtube" />
        </a>
        <a class="SoMe-icon bsky" href="https://bsky.app/profile/masahjor.bsky.social" target="_blank" rel="noopener noreferrer">
            <img src="bsky-logo.png" alt="Bluesky" />
        </a>
        <a class="SoMe-icon github" href="https://github.com/Masahjor" target="_blank" rel="noopener noreferrer">
            <img src="github-logo.png" alt="Github" />
        </a>
        <a class="SoMe-icon cara" href="https://cara.app/masahjor" target="_blank" rel="noopener noreferrer">
            <img src="cara-logo.png" alt="Cara" />
        </a>
    </div>
    <p class="footer-note">
        Built with <a href="https://svelte.dev/" target="_blank" rel="noopener noreferrer" class="sveltekit">SvelteKit</a> & <a href="https://tailwindcss.com/" target="_blank" rel="noopener noreferrer" class="tailwind">Tailwind</a>
    </p>
</div>

<!-- CSS -->
<style>
    @font-face {
        font-family: 'Nexa-Heavy.ttf';
        src: url('Nexa-Heavy.ttf') format('truetype');
    }

    .footer {
        font-family: 'Nexa-Heavy.ttf', sans-serif;
        background: lightgray;
        background: linear-gradient(0deg,rgb(255, 255, 255) 20%, rgba(119, 68, 68, 0) 100%);
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
        transition: color 0.2s ease;
    }

    .sveltekit:hover {
        color: #ffbc14;
    }

    .tailwind {
        color: #3f48cc;
        transition: color 0.2s ease;
    }

    .tailwind:hover {
        color: #4ac8de;
    }
    
    .SoMe-icon {
        transition: transform .2s;
    }
    .SoMe-icon:hover {
        transform: scale(1.5);
    }

    .SoMe-icon.youtube:hover img {
        content: url('youtube-hover-logo.png');
    }

    .SoMe-icon.bsky:hover img {
        content: url('bsky-hover-logo.png');
    }

    .SoMe-icon.github:hover img {
        content: url('github-hover-logo.png');
    }

    .SoMe-icon.cara:hover img {
        content: url('cara-hover-logo.png');
    }

     @media (max-width: 414px) {
        .footer-note {
            display: none;
        }
     }
</style>
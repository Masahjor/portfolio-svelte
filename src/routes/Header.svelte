<!-- script -->
<script lang="ts">
        import { onMount } from 'svelte';
    let sections = [
        { name: 'About Me', path: '/' },
        { name: 'Education', path: '/education' },
        { name: 'Art Gallery', path: '/art-gallery' },
        { name: 'IT Projects', path: '/it-projects' },
        { name: 'FAQ', path: '/faq' }
    ];
    let isMenuOpen = false;

    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }
</script>

<!-- HTML -->
<div class="header">
    <header>
        <figure>
            <!-- svelte-ignore a11y_img_redundant_alt -->
            <img src="Masahjor-Logo.png" alt="My photo" width="250" class="logo-pic">
        </figure>
    </header>

    <!-- Burger Menu -->
    <!-- svelte-ignore a11y_click_events_have_key_events -->
    <!-- svelte-ignore a11y_no_static_element_interactions -->
    <div class="burger-menu" on:click={toggleMenu}>
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
    </div>

    <!-- Navigation -->
    <nav class:open={isMenuOpen}>
        <ul>
            {#each sections as section}
            <li>
                <a href={section.path} on:click={() => (isMenuOpen = false)}>{section.name}</a>
            </li>
            {/each}
        </ul>
    </nav>
</div>

<!-- CSS -->
<style>
    @font-face {
        font-family: 'Nexa-ExtraLight.ttf';
        src: url('Nexa-ExtraLight.ttf') format('truetype');
    }

    .header {
        font-family: 'Nexa-ExtraLight.ttf', sans-serif;
        background: lightgray;
        background: linear-gradient(180deg, rgba(211, 211, 211, 1) 20%, rgba(0, 0, 0, 0) 100%);
        padding: 1em;
        height: auto;
        margin: auto;
        text-align: center; /* Center content inside the header */
    }

    header {
        display: flex;
        align-items: center;
        justify-content: space-between; /* Space between logo and burger menu */
    }

    header figure {
        margin: 0 auto; /* Center the figure element */
        display: inline-block; /* Ensure it doesn't stretch */
    }

    .logo-pic {
        max-width: 100%; /* Ensure responsiveness */
        height: auto;
    }

    nav {
        min-height: 50px;
        position: relative;
        background-color: #333;
        overflow: hidden;
        border-radius: 3px;
        display: flex;
        justify-content: center;
        transition: max-height 0.3s ease;
    }

    nav ul {
        display: flex;
        justify-content: center;
        align-items: center; /* Center nav a tags vertically */
        margin: 0;
        list-style: none;
    }

    nav a {
        border-radius: 5px;
        color: #f2f2f2;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        font-size: 17px;
        transition: transform 0.2s;
    }

    nav a:hover {
        color: lime;
        transform: scale(1.1);
    }

    .burger-menu {
        display: none;
        flex-direction: column;
        justify-content: space-around;
        width: 30px;
        height: 25px;
        cursor: pointer;
        margin: 0 auto;
    }

    .burger-menu .bar {
        width: 100%;
        height: 4px;
        background-color: #333;
        border-radius: 2px;
    }

    nav.open {
        display: block;
    }

    @media (max-width: 414px) {
        .header {
            padding: 0.5em;
        }

        header {
            display: flex;
            align-items: center;
            justify-content: space-between; /* Ensure logo and burger menu are on the same level */
        }

        .logo-pic {
            max-width: 150px;
        }

        .burger-menu {
            display: flex;
        }

        nav {
            flex-direction: column;
            max-height: 0;
            min-height: 0;
            overflow: hidden;
        }

        nav.open {
            max-height: 300px; /* Adjust as needed */
        }

        nav ul {
            flex-direction: column;
            align-items: center; /* Override to keep alignment for phone screens */
        }

        nav a {
            padding: 10px 12px;
            font-size: 28px; /* Increased font size for larger text */
        }
    }
</style>
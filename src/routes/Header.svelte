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
</script>

<!-- HTML -->
<main>
    <header>
        <figure>
            <!-- svelte-ignore a11y_img_redundant_alt -->
            <img src="MshjrUnderskriftV2.png"alt="My photo" width="250" class="profile-pic">
        </figure>
    </header>
<!-- Jeg fucking brøler -->
    <nav>
        <ul>
            {#each sections as section}
            <li>
                <a href={section.path}>{section.name}</a>
            </li>
        {/each}
        </ul>
    </nav>
</main>

<!-- CSS -->
<style>
    @font-face {
        font-family: 'Nexa-ExtraLight.ttf';
        src: url('Nexa-ExtraLight.ttf') format('truetype');
    }

    main {
        font-family: 'Nexa-ExtraLight.ttf', sans-serif;
        background-color: lightgray;
        padding: 1em;
        height: auto;
        margin: auto;
    }


    nav {
        position: relative;
        background-color: #333;
        overflow: hidden;
        border-radius: 3px;
    }

    nav ul {
        display: flex;
        justify-content: center; /* Center the list items */
        padding: 0;
    }

    nav a {
        border-radius: 5px;
        float: left;
        color: #f2f2f2;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        font-size: 17px;
        transition: transform .2s;
    }

    nav a:hover {
        color: lime;
        transform: scale(1.1)
    }

    
</style>
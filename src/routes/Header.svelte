<!-- script -->
<script lang="ts">
    
</script>

<!-- HTML -->
<main>
    <header>
        <figure>
            <!-- svelte-ignore a11y_img_redundant_alt -->
            <img src="evilmads.jpg"alt="My photo" width="20" height="20" class="profile-pic">
        </figure>
    </header>

    <nav>
        <ul>
            <li><a class="active" href="/about">About me</a></li>
            <li><a href="/education">Education</a></li>
            <li><a href="/art">Art Gallery</a></li>
            <li><a href="/it">IT Work</a></li>
        </ul>
    </nav>
</main>

<!-- CSS -->
<style>
    main {
        background-color: hotpink;
        padding: 1em;
        height: auto;
        margin: auto;
    }

    nav {
        position: relative;
        background-color: #333;
        overflow: hidden;
    }

    nav ul {
        display: flex;
        justify-content: center; /* Center the list items */
        padding: 0;
    }

    nav a {
        float: left;
        color: #f2f2f2;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        font-size: 17px;
    }

    nav a:hover {
        background-color: yellow;
        color: black;
    }

    nav a.active {
        background-color: blue;
        color: white;
    }
    
</style>
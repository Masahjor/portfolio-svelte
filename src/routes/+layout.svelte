<script>
// svelte-ignore export_let_unused
    export let data;
</script>

<div class="background"></div>
<slot />

<style>
    .background {
        background-attachment: fixed;
        background-size: cover;
        background-position: center;
        height: 100vh; /* Set to viewport height */
        width: 100%;
        position: fixed;
        top: 0;
        left: 0;
        z-index: -1; /* Ensure it stays behind all content */
        background: url(sketchesMay5th.png) repeat 0 0;
        animation: animate 20s infinite linear;
    }

    @keyframes animate {
        100% {
            background-position: -1024px -512px;
        }
    }
</style>
<!-- ========== Script ========== -->
<script lang="ts">
  import data from './data.json'; // Import the JSON data
</script>

<!-- ========== HTML ========== -->
<div class="main-content">
  <div class="grid-container">

    <!-- 1st row: H1 spanning both columns -->
    <div class="grid-item image-span" style="grid-column: span 2;">
      <!-- Dynamically bind the title from the first section in data.json -->
      <h1>{data.sections[0].title}</h1> 
      <p>{data.sections[0].content}</p>
    </div>

  <div class="grid-item highlight-img phone-span">
    <blockquote class="bluesky-embed " data-bluesky-uri="at://did:plc:3vw7d4df7g6omrwc3ugjvejv/app.bsky.feed.post/3looxndfdgk2u" data-bluesky-cid="bafyreietpnz5zpaozk5hhykiurnxygm7jwwzavobqywexen6r3wprav72m" data-bluesky-embed-color-mode="system"><p lang="en">Dark Buuss and his gf #digitalart #art #pvz #plantsvszombies<br><br><a href="https://bsky.app/profile/did:plc:3vw7d4df7g6omrwc3ugjvejv/post/3looxndfdgk2u?ref_src=embed">[image or embed]</a></p>&mdash; Masahjor (<a href="https://bsky.app/profile/did:plc:3vw7d4df7g6omrwc3ugjvejv?ref_src=embed">@masahjor.bsky.social</a>) <a href="https://bsky.app/profile/did:plc:3vw7d4df7g6omrwc3ugjvejv/post/3looxndfdgk2u?ref_src=embed">May 9, 2025 at 12:30 AM</a></blockquote><script async src="https://embed.bsky.app/static/embed.js" charset="utf-8"></script>
  </div>

  <div class="grid-item highlight-img phone-span">
    <blockquote class="bluesky-embed" data-bluesky-uri="at://did:plc:3vw7d4df7g6omrwc3ugjvejv/app.bsky.feed.post/3lo5aep2wm22c" data-bluesky-cid="bafyreici626k2o4rsvp3szav7sedoxksxwtlyiunadqpjdpfaast2exm3q" data-bluesky-embed-color-mode="system"><p lang="en">Sketch sesh from last night made me make a new original character. Quite fond of Beofre, the charmingly cute cyclops. #oc #originalcharacter #digitalart #blue #sketch<br><br><a href="https://bsky.app/profile/did:plc:3vw7d4df7g6omrwc3ugjvejv/post/3lo5aep2wm22c?ref_src=embed">[image or embed]</a></p>&mdash; Masahjor (<a href="https://bsky.app/profile/did:plc:3vw7d4df7g6omrwc3ugjvejv?ref_src=embed">@masahjor.bsky.social</a>) <a href="https://bsky.app/profile/did:plc:3vw7d4df7g6omrwc3ugjvejv/post/3lo5aep2wm22c?ref_src=embed">May 1, 2025 at 11:19 PM</a></blockquote><script async src="https://embed.bsky.app/static/embed.js" charset="utf-8"></script>
  </div>

    <!-- 2nd row: Image spanning both columns -->
    <div class="grid-item image-span" style="grid-column: span 2;">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src={data.sections[0].image} alt="About me Image" />
    </div>


  </div>
</div>

<!-- ========== CSS ========== -->
<style>
    @font-face {
        font-family: 'Nexa-ExtraLight.ttf';
        src: url('Nexa-ExtraLight.ttf') format('truetype');
        font-family: 'Nexa-Heavy.ttf';
        src: url('Nexa-Heavy.ttf') format('truetype');
        font-family: 'coolvetica rg.oft';
        src: url ('coolvetica rg.oft') format('truetype');
    }

  .main-content {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh; /* Full viewport height */
  }

  .grid-container {
    display: grid;
    /* background: green; */
    grid-template-columns: repeat(2, 1fr); /* Two columns */
    gap: 1rem; /* Adjust gap as needed */
    width: 1000px; /* Full width */
    height: 100%; /* Full height */
  }

  .grid-item {
    background-color: #f0f0f0; /* Example background color */
    padding: 1rem;
    text-align: center;/* border: 1px solid green; */ /* Example border */
    font-family: 'coolvetica rg.oft', sans-serif;

    /* border: 1px solid green; */ /* Example border */
    border-radius: 5px; /* Rounded corners */
    border-style: solid;
    /* font-family: 'Nexa-ExtraLight.ttf', sans-serif; */


    & img {
      max-width: 100%;
      height: auto;
      display: block;
      margin: 0 auto;
    }

  }

  /* Redundant class */
  /* .grid-item-invisible {
    background-color: rgba(185, 230, 117, 0.414);
    border: none;
  } */

  .image-span {
    text-align: center;
  }

  h1 {
    font-family: 'Nexa-Heavy.ttf', sans-serif;
    font-size: 4rem;
  }

  /* Redundant class */
  /* h2 {
    font-family: 'Nexa-Heavy.ttf', sans-serif;
    font-size: 2.5rem;
    color: darkgreen;
  }

  .text-2-left {
    text-align: left;
  } */

  /* Responsive styles for phone screens */
  @media (max-width: 414px) {
    .grid-container {
      grid-template-columns: 1fr; /* Single column layout */
      width: 90%; /* Adjust width for smaller screens */
      background-color: invisible;
    }

    .grid-item {
      padding: 0.5rem; /* Reduce padding for smaller screens */
    }

    h1 {
      font-size: 1.5rem; /* Adjust font size for smaller screens */
    }

    /* Redundant class */
    /* .text-2-left {
      font-size: 0.9rem;
    } */

    .phone-span {
       grid-column: span 2;
    }
  }

  .highlight-img:hover {
    transition: transform 0.3s ease, box-shadow 0.3s ease; /* Smooth transition */
    background-color: limegreen;/* Add a subtle green background */
    transition: background-color 0.3s ease, box-shadow 0.3s ease; /* Smooth transition */
  }

  /* Add keyframes for fade-in */
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(100px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  /* Apply animation to grid items */
  .grid-item {
    opacity: 0; /* Start hidden */
    animation: fadeInUp 0.8s ease-out forwards;
    animation-delay: calc(var(--order) * 0.2s); /* Stagger animation */
  }


  
</style>

<!-- ========== End of code ========== -->
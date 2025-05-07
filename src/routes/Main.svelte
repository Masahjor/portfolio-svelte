<!-- Script -->
<script lang="ts">

</script>

<!-- HTML -->
<div class="main-content">
  <div class="grid-container">

    <!-- First row: H1 spanning both columns -->
    <div class="grid-item image-span" style="grid-column: span 2;">
      <h1>About me</h1>
      <p>Heya, welcome to my portfolio. My name is Masahjor and I'm a software developer of web applications and video games.</p>
    </div>

    <!-- Second row: Image spanning both columns -->
    <div class="grid-item image-span" style="grid-column: span 2;">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src="myBaddies.png" alt="Placeholder Image" />
    </div>

    <!-- Third row -->
    <div class="grid-item" style="grid-column: span 2;">
      <p>Listen fellas, hear me out...</p>
      <p class="text-2-left"> My main hobbies include drawing, going for long walks in natural and urban environments, being evil and rampant maffing.</p>
    </div>

    <!-- Fourth row -->
    <div class="grid-item">
      <h2>Personality</h2>
      <p class="text-2-left">I am committed and focus a lot on my tasks/projects, and think visually. I have lots of humor and when you get to know me, that's when the fun conversations really begin. If you need help with something graphic, I'm almost always ready to help. I dream of an apprenticeship where I can make a difference and be part of a future team where I can contribute with my skills and not least learn a lot. My strongest skills have always been in creativity, language and design. I am a person with high-functioning autism. That means I perceive things and concepts from a perspective that may be different from that of other people.</p>
    </div>
    <div class="grid-item">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src="AlexLogo.png" alt="Placeholder Image" />
    </div>

    <!-- Fifth row -->
    <div class="grid-item">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src="AlexLogo.png" alt="Placeholder Image" />
    </div>
    <div class="grid-item">
      <h2>Skills</h2>
      <p class="text-2-left">The program I work with most often is Clip Studio Paint, it is where I draw 99% of the time when its digital.</p>
      <p class="text-2-left">I have plenty of experience with the majority of apps found in the Adobe package, like fx. Photoshop, Illustrator, InDesign, After Effects and more.</p>
      <p class="text-2-left">I'm also decently skilled at a good chunk of computer languages and frameworks, though my specialty is the Svelte framework and TypeScript language.</p>
      <p class="text-2-left">Over the years I've managed to become very familiar with video editing. Especially when it comes to making effective, fast, shortform entertainment videos.</p>
      <p class="text-2-left">Even though most of my skills require a computer, I'm excellent at working with my hands! Woodworking is a skill I've honed to great lengths, my specialty being homemade furniture construction and designing.</p>
    </div>

    <!-- Sixth row -->
    <div class="grid-item">
      <h2>Life story</h2>
      <p>This is some filler content for the first column in the third row. Add more text or elements as needed.</p>
    </div>
    <div class="grid-item">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src="barbella.jpg" alt="Placeholder Image" />
    </div>
  </div>
</div>

<!-- CSS -->
<style>
    @font-face {
        font-family: 'Nexa-ExtraLight.ttf';
        src: url('Nexa-ExtraLight.ttf') format('truetype');
        font-family: 'Nexa-Heavy.ttf';
        src: url('Nexa-Heavy.ttf') format('truetype');
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
    width: 50%; /* Full width */
    height: 100%; /* Full height */
  }

  .grid-item {
    background-color: #f0f0f0; /* Example background color */
    padding: 1rem;
    text-align: center;/* border: 1px solid green; */ /* Example border */

    /* border: 1px solid green; */ /* Example border */
    border-radius: 5px; /* Rounded corners */
    border-style: solid;

    & img {
      max-width: 100%;
      height: auto;
      display: block;
      margin: 0 auto;
    }
  }

  .image-span {
    text-align: center;
  }

  h1 {
    font-family: 'Nexa-Heavy.ttf', sans-serif;
  }

  .text-2-left {
    text-align: left;
  }

  /* Responsive styles for phone screens */
  @media (max-width: 414px) {
    .grid-container {
      grid-template-columns: 1fr; /* Single column layout */
      width: 90%; /* Adjust width for smaller screens */
      background-color: green;
    }

    .grid-item {
      padding: 0.5rem; /* Reduce padding for smaller screens */
    }

    h1 {
      font-size: 1.5rem; /* Adjust font size for smaller screens */
    }

    .text-2-left {
      font-size: 0.9rem; /* Adjust text size for readability */
    }
  }

  .grid-item img[src="AlexLogo.png"]:hover {
    transform: scale(1.1); /* Slightly enlarge the image */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Add a subtle shadow */
    transition: transform 0.3s ease, box-shadow 0.3s ease; /* Smooth transition */
  }
</style>
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

    <!-- 2nd row: Image spanning both columns -->
    <div class="grid-item image-span" style="grid-column: span 2;">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src={data.sections[0].image} alt="Placeholder Image" />
    </div>

    <!-- 3rd row -->
    <div class="grid-item" style="grid-column: span 2;">
      <p>{data.sections[1].content1}</p>
      <p class="text-2-left">{data.sections[1].content2}</p>
    </div>

    <!-- 4th row -->
    <div class="grid-item grid-item-invisible" style="grid-column: span 2;">
      <h2>{data.sections[2].title}</h2>
    </div>
    
    <!-- 5th row -->
    <div class="grid-item">
      <p class="text-2-left">{data.sections[2].content}</p>
    </div>
    <div class="grid-item highlight-img">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src={data.sections[2].image} alt="Personality Image" />
    </div>

    <!-- 6th row -->
    <div class="grid-item grid-item-invisible" style="grid-column: span 2;">
      <h2>{data.sections[3].title}</h2>
    </div>

    <!-- 7th row -->
    <div class="grid-item highlight-img">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src={data.sections[3].image} alt="Skills Image" />
    </div>
    <div class="grid-item">
      <p class="text-2-left">{data.sections[3].content}</p>
    </div>

    <!-- 8th row -->
    <div class="grid-item grid-item-invisible" style="grid-column: span 2;">
      <h2>{data.sections[4].title}</h2>
    </div>
    <div class="grid-item">
      <p class="text-2-left">{data.sections[4].content}</p>
    </div>
    <div class="grid-item highlight-img">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src={data.sections[4].image} alt="Life Story Image"/>
    </div>

    <!-- 9th row -->
    <div class="grid-item grid-item-invisible" style="grid-column: span 2;">
      <h2>HEOW</h2> <!-- {data.sections[5].title} -->
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

  .grid-item-invisible {
    background-color: rgba(185, 230, 117, 0.414); /* Make this item invisible */
    border: none; /* Remove border */
  }

  .image-span {
    text-align: center;
  }

  h1 {
    font-family: 'Nexa-Heavy.ttf', sans-serif;
    font-size: 4rem;
  }

  h2 {
    font-family: 'Nexa-Heavy.ttf', sans-serif;
    font-size: 2.5rem;
    color: darkgreen;
  }

  .text-2-left {
    text-align: left;
  }

  /* Responsive styles for phone screens */
  @media (max-width: 414px) {
    .grid-container {
      grid-template-columns: 1fr; /* Single column layout */
      width: 90%; /* Adjust width for smaller screens */
      background-color: hotpink;
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
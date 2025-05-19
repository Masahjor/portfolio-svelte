<!-- ========== Script ========== -->
 <script lang="ts">
    import data from './data.json'; // Import the JSON data
 </script>

<!-- ========== HTML ========== -->
<div class="main-content">
    <div class="grid-container">

        <div class="grid-item image-span" style="grid-column: span 2;">
            <h1>{data.sections[0].title}</h1>
            <p>{data.sections[0].content}</p>
        </div>

        <div class="grid-item image-span" style="grid-column: span 2;">
            <img src={data.sections[0].image} alt="projects img" />
        </div>

        <div class="grid-item grid-item-opaque item-invisible" style="grid-column: span 2;">
            <p class="item-invisible">Secret text :)</p>
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

  .grid-item-opaque {
    background-color: rgba(185, 230, 117, 0.414); /* Make this item transparent */
    border: none; /* Remove border */
  }

  .item-invisible {
    background-color: rgba(185, 230, 117, 0);
    color: rgba(185, 230, 117, 0);
    border: none;
    min-height: 120px;
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
      background-color: invisible;
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
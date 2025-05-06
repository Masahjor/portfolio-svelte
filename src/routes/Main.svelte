<!-- Script -->
<script lang="ts">

</script>

<!-- HTML -->
<div class="main-content">
  <div class="grid-container">
    <!-- First row -->
    <div class="grid-item">
      <h2>Column 1</h2>
      <p>This is some filler content for the first column. You can add more text or elements here.</p>
    </div>
    <div class="grid-item">
      <h2>Column 2</h2>
      <p>This is some filler content for the second column. Feel free to customize it as needed.</p>
    </div>

    <!-- Second row: Image spanning both columns -->
    <div class="grid-item image-span" style="grid-column: span 2;">
      <!-- svelte-ignore a11y_img_redundant_alt -->
      <img src="airaccal.png" alt="Placeholder Image" />
    </div>

    <!-- Third row -->
    <div class="grid-item">
      <h2>Column 1 (Row 3)</h2>
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
  .main-content {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh; /* Full viewport height */
  }

  .grid-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr); /* Two columns */
    gap: 1rem; /* Adjust gap as needed */
    width: 50%; /* Full width */
    height: 100%; /* Full height */
  }

  .grid-item {
    background-color: #f0f0f0; /* Example background color */
    padding: 1rem;
    text-align: center;
    border: 1px solid #ccc; /* Example border */
  }

  .grid-item img {
    max-width: 100%;
    height: auto;
    display: block;
    margin: 0 auto;
  }

  .image-span {
    text-align: center;
  }
</style>
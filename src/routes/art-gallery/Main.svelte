<!-- Script -->
<script lang="ts">

</script>

<!-- HTML -->
<div class="main-content">  
  <div class="grid-container">
    <div class="grid-item">ZA WARUDO</div>
    <div class="grid-item">TOKI WO TOMARE</div>
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
</style>
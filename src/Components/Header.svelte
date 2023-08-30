<script>
  export let cars = ["Supercars", "Hypercars", "Roadsters", "Volchrons"];
</script>

<header>
  <div class="grid">
    {#each cars as car}
      <div class="car">{{ car }}</div>
    {/each}
  </div>
</header>

<style>
  header {
  }

  .grid {
    display: grid;
    grid-template-areas: "cars";
    grid-template-columns: 3fr repeat(4, 1fr);
    grid-template-rows: 1fr;
    align-items: center;
    justify-items: center;
  }

  .car {
    border: 1px solid black;
    padding: 1rem;
  }
</style>

<script lang="ts">
  const products = [
    {
      id: 1,
      name: "Dog",
      price: 14.99,
    },
    {
      id: 2,
      name: "Cat",
      price: 14.99,
    },
    {
      id: 3,
      name: "Fish",
      price: 14.99,
    },
  ];
</script>

<main>
  <h1>Products</h1>

  <div class="grid">
    {#each products as product}
      <div>
        <h2>{product.name}</h2>
        <p>Price: ${product.price}</p>
      </div>
    {/each}
  </div>
</main>

<style>
  main {
    margin: 0 auto;
    max-width: 54em;
  }

  .grid {
    display: grid;
    grid-gap: 1em;
    margin-bottom: 5em;
    grid-template-columns: repeat(3, 1fr);
  }

  h1 {
    padding-bottom: 0.5em;
    border-bottom: 2px dotted black;
  }

  button {
    width: 100%;
    padding: 0.5em 1em;
  }
</style>

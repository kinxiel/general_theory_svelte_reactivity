<script>
  let count = 0;

  const increment = () => {
    count += 1;
  };

  const decrement = () => {
    count -= 1;
  };
</script>

<div class="container">
  <button on:click={decrement}> - </button>
  <div class="count">
    {count}
  </div>
  <button on:click={increment}> + </button>
</div>

<style>
  .container {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0.8rem;
    border: solid 1px #ccc;
    border-radius: 5px;
    width: 10%;
  }

  .count {
    padding: 1rem;
    margin-bottom: 0.5rem;
  }
</style>

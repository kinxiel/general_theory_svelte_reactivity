<script>
  let numbers = [1, 2, 3];

  const addNumber = () => {
    numbers.push(numbers.length + 1);
    console.log(numbers);
    numbers = numbers;
  };
</script>

{#each numbers as number}
  <p>
    {number}
  </p>
{/each}

<button on:click={addNumber}> Add a number </button>

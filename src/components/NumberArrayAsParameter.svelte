<script>
  let numbers = [1, 2, 3];
  $: console.log(numbers);

  const addNumber = (arr) => {
    arr.push(arr.length + 1);
    console.log(arr);
    numbers = numbers;
  };
</script>

{#each numbers as number}
  <p>
    {number}
  </p>
{/each}

<button
  on:click={() => {
    addNumber(numbers);
  }}
>
  Add a number
</button>

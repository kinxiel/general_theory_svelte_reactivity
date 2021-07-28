<script>
  let numbers = [1, 2, 3];
  let isVisible = true;

  function addNumber() {
    numbers.push(numbers.length + 1);
    console.log(numbers);
  }

  function rerender() {
    isVisible = false;
    setTimeout(function () {
      isVisible = true;
    }, 100);
  }
</script>

{#if isVisible}
  {#each numbers as number}
    <p>
      {number}
    </p>
  {/each}
{/if}

<button on:click={addNumber}> Add a number </button>
<button on:click={rerender}> Rerender </button>

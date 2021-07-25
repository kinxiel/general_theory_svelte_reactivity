<script>
  const getMean = (arr) => {
    let mean =
      arr.reduce((accumulator, currentValue) => {
        return accumulator + currentValue;
      }, 0) / arr.length;

    return mean;
  };

  const getStandardDeviation = (arr) => {
    // (value - mean)^2
    let innerArray = arr.map((x) => {
      return (x - getMean(arr)) ** 2;
    });

    // Summation
    let sumInnerArray = innerArray.reduce(
      (accumulator, currentValue) => accumulator + currentValue,
      0
    );

    // Calculate the variance (sample standard deviation)
    let variance = sumInnerArray / (arr.length - 1);

    // Standard deviation
    return Math.sqrt(variance);
  };

  let inputArray = '';

  $: numericArray = inputArray.split(',').map((number) => {
    return parseFloat(number, 10);
  });

  $: mean = getMean(numericArray);
  $: stdev = getStandardDeviation(numericArray);
  $: relstdev = stdev / mean;
</script>

<div>
  <label for="list_of_numbers"> Enter a comma separated list of numbers </label>
  <input
    name="list_of_numbers"
    id="list_of_numbers"
    type="text"
    placeholder="Comma separated list"
    bind:value={inputArray}
  />
</div>

<div class="container">
  <div>
    Average: {mean}
  </div>
  <div>
    Standard Deviation: {stdev}
  </div>
  <div>
    Rel Standard Deviation: {relstdev}
  </div>
</div>

<style>
  #list_of_numbers {
    padding: 0.8rem;
    margin: 0.5rem;
  }

  .container {
    display: inline-flex;
    flex-direction: column;
    margin-top: 0.3rem;
  }

  .container > div {
    margin: 0.3rem;
  }
</style>

<script>
  import Counter from './components/Counter.svelte';
  import Input from './components/Input.svelte';
  import InputBroken from './components/InputBroken.svelte';
  import InputFixed from './components/InputFixed.svelte';
  import NumberArray from './components/NumberArray.svelte';
  import NumberArrayReassignment from './components/NumberArrayReassignment.svelte';
  import NumberArraySpread from './components/NumberArraySpread.svelte';
  import NumberArrayAsParameter from './components/NumberArrayAsParameter.svelte';
  import NumberArrayRerender from './components/NumberArrayRerender.svelte';
  import RelativeStandardDeviation from './components/RelativeStandardDeviation.svelte';
</script>

<main>
  <h3>Counter</h3>
  <Counter />
  <br />

  <h3>Input</h3>
  <Input />
  <br />

  <h3>Broken Input</h3>
  <InputBroken />
  <br />

  <h3>Fixed Input</h3>
  <InputFixed />
  <br />

  <h3>Relative Standard Deviation</h3>
  <RelativeStandardDeviation />
  <br />

  <h3>NumberArray (not working)</h3>
  <NumberArray />
  <br />

  <h3>NumberArray Reassignment</h3>
  <NumberArrayReassignment />
  <br />

  <h3>NumberArray Spread Operator</h3>
  <NumberArraySpread />
  <br />

  <h3>NumberArray as Parameter</h3>
  <NumberArrayAsParameter />
  <br />

  <h3>Rerender</h3>
  <NumberArrayRerender />
</main>

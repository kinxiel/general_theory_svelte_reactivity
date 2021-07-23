<script>
  let textValue = '';
  let charCount = textValue.length;
</script>

<div class="container">
  <div>
    <label for="text_input">Text Input</label>
    <input
      id="text_input"
      name="text_input"
      type="text"
      placeholder="input text here"
      bind:value={textValue}
    />
  </div>
  <div>
    Uppercase:{textValue.toUpperCase()}
  </div>
  <div>
    Characters: {charCount}
  </div>
</div>

<style>
  .container {
    display: flex;
    flex-direction: column;
  }

  label {
    padding: 0.2em;
  }
</style>

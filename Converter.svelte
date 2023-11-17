<script>
  let inches = "1";
  let centimeters = "2.54";

  const convertToCm = () => {
    const inchValue = parseFloat(inches);
    if (!isNaN(inchValue)) {
      const cmValue = inchValue * 2.54;
      centimeters = cmValue.toFixed(2);
    } else {
      centimeters = "";
    }
  };

  const convertToInches = () => {
    const cmValue = parseFloat(centimeters);
    if (!isNaN(cmValue)) {
      const inchValue = cmValue / 2.54;
      inches = inchValue.toFixed(2);
    } else {
      inches = "";
    }
  };
</script>

<div class="container">
  <div>
    <input type="number" bind:value={inches} on:input={convertToCm} />
    <span class="text">inch</span>
  </div>
  <div>
    <input type="number" bind:value={centimeters} on:input={convertToInches} />
    <span class="text">cm</span>
  </div>
</div>

<style>
  .container {
    display: flex;
    flex-direction: column;
    gap: 10px;
    font-size: 28px;
  }
  input {
    font-size: 1em;
    text-align: right;
    border: 1px solid #ccc;
    border-radius: 5px;
    background: none;
    padding: 2px 46px 2px 6px;
    margin: 0;
    width: 230px;
    height: 40px;
  }
  .text {
    display: inline-block;
    font-size: 0.6em;
    text-align: right;
    margin-left: -42px;
    padding: 0;
  }

  @media (min-width: 480px) {
    input {
      width: 160px;
    }
  }

  /* Chrome, Safari, Edge, Opera */
  input::-webkit-outer-spin-button,
  input::-webkit-inner-spin-button {
    -webkit-appearance: none;
    margin: 0;
  }

  /* Firefox */
  input[type="number"] {
    -moz-appearance: textfield;
  }
</style>
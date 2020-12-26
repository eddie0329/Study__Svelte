<script>
  let numbers = [1, 2, 3, 4];

  $: sumOfNumbers = numbers.reduce((a, c) => a + c);

  const addNumber = () => {
    numbers = [...numbers, numbers.length + 1];
  };
</script>

<h1>NUMBERS: {numbers}</h1>
<h1>SUM: {sumOfNumbers}</h1>
<button on:click={addNumber}>ADD</button>

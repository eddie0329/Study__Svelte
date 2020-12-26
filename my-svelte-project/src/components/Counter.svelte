<script>
  let count = 0;

  const increaseCount = () => {
    count += 1;
  };

  const decreaseCount = () => {
    count -= 1;
  };

  $: double = count * 2;
  $: console.log(`count is ${count}`);
  $: if (count === 10) {
    console.log(`count is 10`);
  }
</script>

<h1>{count}</h1>
<h1>{double}</h1>
<button on:click={increaseCount}>+</button>
<button on:click={decreaseCount}>-</button>

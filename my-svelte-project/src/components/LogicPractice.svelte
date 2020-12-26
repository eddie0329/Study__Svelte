<script>
  let count = 0;

  const onClickPlus = () => {
    count++;
  };
</script>

<h1>COUNT: {count}</h1>
{#if count === 0}
  <div>count is zero</div>
{:else if count % 2}
  <div>count is odd</div>
{:else}
  <div>count is even</div>
{/if}

<button on:click={onClickPlus}>PLUS</button>

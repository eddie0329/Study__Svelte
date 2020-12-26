<script>
  const count = {
    num: 0,
  };

  const onPlus = () => {
    count.num++;
  };
</script>

<h1>{count.num}</h1>
<button on:click={onPlus}>PLUS</button>

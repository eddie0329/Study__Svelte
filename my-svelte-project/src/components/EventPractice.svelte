<script>
  const onClick = () => {
    console.log('HELLO');
  };
</script>

<button on:click|once={() => { console.log('HELLO') }}>HELLO</button>

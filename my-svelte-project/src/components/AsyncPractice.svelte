<script>
  import axios from 'axios';

  let users;

  const getUsers = async () => {
    try {
      const res = await axios.get('https://jsonplaceholder.typicode.com/users');
      users = res.data;
      return res;
    } catch(error) {
      throw new Error(error);
    }
  }
  let promise = getUsers();
</script>

{#await promise}
  <h1>...LOADING</h1>
{:then}
  <ul>
    {#each users as {name, username}}
    <li>
      <span>name: {name}</span>
      <span>username: {username}</span>
    </li>
    {/each}
  </ul>
{:catch error}
  <h1>ERROR: {error.message}</h1>
{/await}

<hr />

{#await promise then value}
  <div>{value}</div>
{/await}

<script>
  let students = [
    { id: 1, name: "eddie" },
    { id: 2, name: "sam" },
    { id: 3, name: "cindy" },
  ];
</script>

<h1>STUDENTS</h1>
<ul>
  {#each students as student, i}
    <li>
      {i}:
      <b>{student.name}</b>
    </li>
  {/each}
</ul>

<ul>
  {#each students as {name, id}, i (id)}
    <li>
      {i}:
      <b>{name}</b>
    </li>
  {/each}
</ul>

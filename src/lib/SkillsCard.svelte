<script>
  export let title;
  export let skills;
</script>

<div class="card">
  <h2>{title}</h2>
  <ul>
    {#each skills as skill}
      <li>{skill}</li>
    {/each}
  </ul>
</div>

<style>
  h2 {
    color: #bfa181;
  }
</style>
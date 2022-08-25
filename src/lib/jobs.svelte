<script>
  import { onMount } from "svelte";
  const url = "https://api.github.com/repos/rebase-network/who-is-hiring/issues?per_page=10&page=1"

  let jobs = [];

  const opts =  {
    'Content-Type': 'application/json'
  }

  onMount(async function () {
    const resp = await fetch(url, {headers: opts});
    console.log("resp.status"  + resp.status)
    const data = await resp.json();
    jobs = data;
  });

</script>


<svelte:head>
  <title>Rebase Jobs</title>
</svelte:head>

<main class="container">
  <div class="list-group w-auto">
    {#each jobs as item}
      <a target="_blank" href="{item.html_url}" class="list-group-item list-group-item-action d-flex gap-3 py-3" aria-current="true">

        <img src="{item.user.avatar_url}" alt="" width="32" height="32" class="rounded-circle flex-shrink-0">

        <div class="d-flex gap-2 w-100 justify-content-between">
          <div>
            <h6 class="mb-0">{item.title}</h6>
            <p class="mb-0 opacity-75"></p>
          </div>
          <small class="opacity-50 text-nowrap">{item.created_at}</small>
        </div>
      </a>
    {/each}
  </div>
  <br/>
  <br/>
</main>


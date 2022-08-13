<script>
  import { onMount } from "svelte";
  // const endpoint = "https://jsonplaceholder.typicode.com/posts";
  const url = "http://db.rebase.network/web3daily/public/posts?_order=-id,-time&_page_size=10&_page=1"

  let posts = [];

  const opts =  {
    'Content-Type': 'application/json'
  }

  onMount(async function () {
    const response = await fetch(url, {headers: opts});
    console.log("response.status"  + response.status)
    const data = await response.json();
    posts = data;
  });

</script>

<svelte:head>
  <title>Rebase Web3Daily</title>
</svelte:head>

<div class="list-group list-group-checkable d-grid gap-2 border-0 w-auto">
  <div>
    <p></p>
  </div>

  {#each posts as post}
    <div class="list-group-item rounded-3 py-3">
      {post.title}
      <span class="small opacity-50">{post.time}</span>
      <a class="d-block small opacity-50" href="{post.url}">{post.title}</a>
      <p>{post.author}：{post.introduce}</p>
    </div>
  {/each}

</div>
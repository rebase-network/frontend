<script>
  import { Router, Route, Link } from "svelte-navigator";

  import svelteLogo from './assets/svelte.svg'
  import Daily from './lib/web3daily.svelte'
  import Jobs from './lib/jobs.svelte'
</script>

<div class="container">
  <Router>

  <header class="d-flex flex-wrap align-items-center justify-content-center justify-content-md-between py-3 mb-4 border-bottom">
    <a href="/" class="d-flex align-items-center col-md-3 mb-2 mb-md-0 text-dark text-decoration-none">
      <img src="{svelteLogo}"/>
    </a>

    <ul class="nav col-12 col-md-auto mb-2 justify-content-center mb-md-0">
      <li><a href="/" class="nav-link px-2 link-secondary">Home</a></li>
      <li><a href="/web3daily" class="nav-link px-2 link-dark">Web3Daily</a></li>
      <li><a href="/jobs" class="nav-link px-2 link-dark">Jobs</a></li>
      <li><a href="#" class="nav-link px-2 link-dark">Events</a></li>
      <li><a href="#" class="nav-link px-2 link-dark">Videos</a></li>
    </ul>

    <div class="col-md-3 text-end">
      <button type="button" class="btn btn-outline-primary me-2">Login</button>
      <button type="button" class="btn btn-primary">Sign-up</button>
    </div>
  </header>

    <Route path="web3daily">
      <Daily />
    </Route>

    <Route path="jobs">
      <Jobs />
    </Route>
  </Router>
</div>

<style>

</style>

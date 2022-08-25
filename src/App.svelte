<script>
  import { Router, Route, Link } from "svelte-navigator";

  import svelteLogo from './assets/svelte.svg'
  import Daily from './lib/web3daily.svelte'
  import Jobs from './lib/jobs.svelte'
</script>
<style>
</style>

<div class="container">
  <Router>
    <Route path="web3daily">
      <Daily />
    </Route>

    <Route path="jobs">
      <Jobs />
    </Route>

    <nav class="navbar navbar-expand-md mb-4">
      <div class="container-fluid">
        <a class="navbar-brand" href="/"> 
          <img src="{svelteLogo}"/>
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarCollapse" aria-controls="navbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarCollapse">
          <ul class="navbar-nav me-auto mb-2 mb-md-0">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="/">Home</a>
            </li>
            <li class="nav-item">
              <a href="/web3daily" class="nav-link px-2 link-dark">Web3Daily</a>
            </li>
            <li class="nav-item">
              <a href="/jobs" class="nav-link px-2 link-dark">Jobs</a>
            </li>
            <li>
              <a href="#" class="nav-link px-2 link-dark">Events</a>
            </li>
            <li>
              <a href="#" class="nav-link px-2 link-dark">Videos</a>
            </li>
          </ul>
          <div class="d-flex">
            <button type="button" class="btn btn-outline-primary me-2">Login</button>
            <button type="button" class="btn btn-primary">Sign-up</button>
          </div>
        </div>
      </div>
    </nav>
  </Router>
</div>


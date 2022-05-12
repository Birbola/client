<script lang="ts">
	import Home from "./pages/home.svelte";
	import { Router, Route, Link} from "svelte-navigator"
</script>

<Router>
<main class="w-100 p-0">
	<div class="navbar bg-base-100 w-100 text-white shadow-lg shadow-green-500/50">
		<div class="flex-none">
			<div class="dropdown">
				<label tabindex="0" class="btn btn-ghost btn-circle">
					<svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h7" /></svg>
				</label>
				<ul tabindex="0" class="menu menu-compact dropdown-content mt-3 p-2 shadow bg-base-100 rounded-box w-52">
					<li><Link to="/">Homepage</Link></li>
					<li><a>About</a></li>
					<li><a>Projects</a></li>
				</ul>
			</div>
		</div>
		<div class="flex-1">
			<a class="nav-link btn btn-ghost normal-case text-xl">Javohir Otanazarov</a>
		</div>
		<div class="flex-none">
      <label tabindex="0" class="btn btn-ghost btn-circle avatar">
        <div class="w-10 rounded-full">
          <img src="https://images.pexels.com/photos/2379005/pexels-photo-2379005.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500" />
        </div>
      </label>
		</div>
	</div>
</main>

<Route path="/" component={Home}></Route>
</Router>

<style>
	.navbar{
		padding: 5px 15px;
	}
	@media (max-width:450px) {
		.navbar{
			padding: 5px 10px;
		}
		.nav-link{
			padding: 0;
		}
	}
</style>
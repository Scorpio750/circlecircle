<script>
	import { Router, Route } from 'svelte-routing';
  import Home from '../Home.svelte';
	import Chananigans from '../Chananigans.svelte';
	import CatDance from '../CatDance.svelte';
	import Betty from '../Betty.svelte';

	export let url = '';
</script>

<Router {url}>
  <div>
    <Route path="betty" component={Betty} />
    <Route path="chananigans" component={Chananigans} />
    <Route path="catdance" component={CatDance} />
    <Route path="/" component={Home} />
  </div>
</Router>

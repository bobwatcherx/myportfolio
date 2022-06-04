<script>
import {Router,Link,Route} from 'svelte-routing';
  import Home from './Home.svelte';
  import Tentang from './pages/Tentang.svelte';
  import Project from './pages/Project.svelte';
  import {flagroute} from './store/store.js';


  export let url = "";

</script>

<Router url="{url}">

  <div>
    <Route path="/" component="{Home}"/>
    <Route path="/about" component="{Tentang}"/>
    <Route path="/project" component="{Project}"/>
  </div>
</Router>

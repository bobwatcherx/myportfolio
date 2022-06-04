<script >
  import Nav from '../lib/Nav.svelte';
	import Man from '../assets/main.jpg'

</script>
<div style="margin-top:20px;z-index: 100;" >
<div class="row">
	<div class="col-sm-12 col-md-12 col-lg-12">
		<Nav/>
	</div>
</div>
<div class="container">
	<div class="row" >
	<div class="col-sm-12 col-md-5 col-lg-6">
		<div class="card">
			<img src={Man} alt="">
		</div>
     
	</div>
	<div class="col-sm-12 col-md-5 col-lg-6">
		<div class="card">
			<img src={Man} alt="">
		</div>
     
	</div>
</div>
</div>
</div>
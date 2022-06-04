<script>
	import Svgcontact from './Svgcontact.svelte';
import guthub from '../assets/github.png';
import yt from '../assets/youtube.png';
import ig from '../assets/ig.png';
</script>

<div>
<div class="row">
	<div class="col-sm-12 col-md-12 col-lg-12">
<Svgcontact/>
		
	</div>
</div>
<div class="row bgcontact">
	<div class="col-sm-12 col-md-12 col-lg-12">
		
<h1 style="
		font-weight: bold;
">Tentang Saya</h1>	
	<div class="blockquote">
			<i>"Sri Edy Nurcahyo, or commonly called Edy. 23 years old, started liking the world of software development since high school, I can develop mobile and web apps"</i>
	</div>
	</div>
</div>
<div class="row"
style="background-color: #A04B2F;" 
>
	<div class="col-sm-2 col-xs-2 col-md-4 col-lg-4">
		<div class="cardinfo">
				<img src={yt} alt=""
	style="height:40px;width:40px"
	/>
		<h6>Sri Edy Nurcahyo</h6>

		</div>
	</div>
	<div class="col-sm-2 col-xs-2  col-md-4 col-lg-4">
		<div class="cardinfo">
				<img src={guthub} alt=""
	style="height:40px;width:40px"
	/>
		<h6>github.com/bobwatcherx</h6>
		</div>
	</div>
	<div class="col-sm-2 col-xs-2  col-md-4 col-lg-4">
		<div class="cardinfo">
				<img src={ig} alt=""
	style="height:40px;width:40px"

	/>
	<h6>eddoyy_or_</h6>
		</div>
	</div>
</div>
</div>


<style>
@import url('https://fonts.googleapis.com/css2?family=Kdam+Thmor+Pro&display=swap');
.cardinfo{
	background-color: white;
	border-radius: 30px;
	display: flex;
	flex-direction: row;
	padding: 10px;
	justify-content: center;
	gap: 10px;
}
.cardinfo h6 {
	font-weight: bold;
	text-align: center;
}
	.bgcontact{
		background-color: #A04B2F;
		padding: 30px;
		color: white;
  	font-family: 'Kdam Thmor Pro', sans-serif;
	}
	.blockquote{
		font-size: 18px;
	}
</style>
<script >
  import Nav from './lib/Nav.svelte';
  import Jumbo from './lib/Jumbo.svelte';
  import Contact from './lib/Contact.svelte';
  import avatar from './assets/main.jpg';
  import arrowup from './assets/arrow.png';
  import { Button } from 'sveltestrap';
  import {onMount} from 'svelte';
  let posproject = [];
  import {datajson} from './loader/data.js';
  onMount(()=>{
    console.log(datajson);
  })

  let y
</script>
<svelte:window bind:scrollY={y} />
<div  style="margin-top:20px">
  <Nav />
  <div class="row container" style="margin-top: 30px;">
    <div class="col-sm-12 order-12 col-md-5 col-lg-5 offset-lg-3" >
     <div class="animationtext">
       <h5>Hi,<br/>I'am <span style="color:#469EF6">Edy</span>
        <br/>
        Web Developer
      </h5>
      <div class="btnprojects">Lihat Projects</div>
     </div>
    </div>
    <div class="col-sm-12 order-1 col-md-5 col-lg-4">
      <div class="animationtextright">
        <div>

            <img src={avatar}
            style="border-radius: 100%;
            height:250px;
            " />
        </div>

      </div>
    </div>

  </div>
  <div class="row">
    <div class="col-sm-12 col-md-12 col-lg-12">
      <div class="row">
  <div class="col-sm-12 .col-md-12 .col-lg-12">
    <svg
     xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#ffd700" fill-opacity="1" d="M0,64L24,85.3C48,107,96,149,144,176C192,203,240,213,288,229.3C336,245,384,267,432,250.7C480,235,528,181,576,144C624,107,672,85,720,112C768,139,816,213,864,218.7C912,224,960,160,1008,154.7C1056,149,1104,203,1152,234.7C1200,267,1248,277,1296,245.3C1344,213,1392,139,1416,101.3L1440,64L1440,320L1416,320C1392,320,1344,320,1296,320C1248,320,1200,320,1152,320C1104,320,1056,320,1008,320C960,320,912,320,864,320C816,320,768,320,720,320C672,320,624,320,576,320C528,320,480,320,432,320C384,320,336,320,288,320C240,320,192,320,144,320C96,320,48,320,24,320L0,320Z"></path></svg>
  </div>
</div>
<!-- content -->
<div class="row " >
  <div class="col-sm-12 col-md-12 col-lg-12">
   <div  style="margin:30px">
      <h1 style="color:black;
      font-family: 'Righteous', cursive;
      ">Projects</h1>
   </div>
  </div>
</div>

    </div>
  </div>
<!-- waves -->
<div class="row " style="margin-top:20px">
          {#each datajson as d}
  <div class="col-sm-6 col-md-4 col-lg-3">
      <div class="card">
      <img src={d.img}/>
      <h3>
      {d.title}
      </h3>
        <div class="cardaction"
        >
        <span style="color:lighblue">{d.type}</span>
          <a href="#" style="
          font-weight: bold;
          text-decoration: none;color:green">Github</a>
        </div>
      </div>
  </div>
      {/each}
</div>
<Contact/>

{#if y !== 0}
<div  class="fab">
  <img src={arrowup} alt=""
  style="height:80px"/>
</div>
{/if}
<!-- end div -->
  </div>

<style >
  @import url('https://fonts.googleapis.com/css2?family=Righteous&display=swap');
@keyframes fabanimation{
  from{
    display: none;
    transform: scale(0);
  }

  to{
    transform: scale(1);
  }
}
 .fab{
  background-color: orange;
  border-radius: 80%;
  color: black;
  width: 80px;
  position: fixed;
  right: 40px;
  bottom: 20px;
  animation-name: fabanimation;
  animation-duration: 0.5s;
 }
  h5{
    font-family: 'Righteous', cursive;
    font-size: 40px;
  }
.card{
  border: 1px solid orange;
  box-shadow: 0px 25px 45px rgb(111,52,108);
  padding: 10px;
  border-radius: 30px;
  display: flex;
  flex-direction: column;
  margin: 10px;
}
 .card h3{
  font-weight: bold;
  font-size: 20px;
  color: grey;
}
.cardaction{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  gap: 10px;
}

  .btnprojects{
    font-family: 'Righteous', cursive;
    background-color: #F3BE14;
    font-size: 20px;
    text-align: center;
    border-radius: 10px;
    box-shadow: 0px 15px 40px rgb(152, 193, 234);
    height: 40px;
    width: 200px;
    padding: 10px;
  }
  .btnprojects:active{
    transform: scale(0.9);
  }
  .bgmain{
  }
  .floatbtn{
    box-shadow: 0px 5px 50px rgba(0,0,0,0.5);
    border-radius: 100%;
    background-color: #FFCE02;
    color: black;
    height: 40px;
    max-width: 80px;
    padding: 10px;
    text-align: center;
    position: fixed;
    right: 20px;
    bottom: 30px;
  }
  .animationtext{
    animation-name: jumboanimation;
    animation-duration: 1s;
  }
  .animationtextright{
    animation-name: righttext;
    animation-duration: 3s;
  }
  @keyframes righttext{
    0% {
      display: none;
      opacity: 0;
      transform: translateX(100px);
    }
    100% {
      opacity:1;
      transform: translateX(0px);
       }
  }
   @keyframes jumboanimation{
    0% {
      display: none;
      opacity: 0;
      transform: translateY(100px);
    }
    100% {
      opacity:1;
      transform: translateY(0px);
       }
  }
</style>
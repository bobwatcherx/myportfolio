<script>
    import { navigate } from "svelte-routing";

   let intpage = 1;
  import iglogo from '../assets/ig.png';
</script>
<div class="row ">
  <div class="col-sm-12 col-xl-12 col-md-12 col-lg-12">
    <div style="display: flex;justify-content: space-around;">
      <div>
        <img src={iglogo} alt=""
      style="width:20px;height:20px"
      >
      eddoyy_or_
      </div>
      <nav class="bgnav"
      >
       <h6 on:click={()=>{
    navigate("/")
        intpage = 1

      }
      }
    class:selected="{intpage == 1}"
        >Home</h6>
  <h6 on:click={()=>{
    navigate("/about")
    intpage = 2;
    }
  }
    class:selected="{intpage == 2}"
    >Tentang</h6>
  <h6 on:click={()=>{
    navigate("/project")
    intpage = 3;

  }
  }
    class:selected="{intpage == 3}"
    >Project</h6>
    </nav>
    </div>
  </div>
</div>
<style>
@import url('https://fonts.googleapis.com/css2?family=Kdam+Thmor+Pro&display=swap');

.gantiwarna{

}

.bgnav{
  font-family: 'Kdam Thmor Pro', sans-serif;
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  gap: 20px;
  font-size: 25px;
}
.bgnav:hover{
  cursor: grabbing;
}
  .selected{
    color: orange;
    font-weight: bold;
  }

</style> 
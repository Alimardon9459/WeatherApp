<template>
  <div>
    <div>

    <div class="page">

      </div>
      <div class=" row justify-center contanier-page wrap ">
        <div v-if=" typeof weather.main != 'undefined' " class=" content col-11 q-mt-lg ">
           <div class="q-mr-lg q-ml-lg q-mt-lg row justify-between">
            <span style="font-size: 32px; color: black;" >
              AVVAL
            </span>
             <span style="font-size: 20px; color: #FFFFFF;">
              18.04.2022
            </span>
           </div>
           <div class="row ">
             <div class="q-ma-lg big-icon">

             </div>
             <div class="q-mt-lg temp-info">
               <span class="big-temp">Harorat:{{weather.main.temp}}ºC</span><br>
               <span class="big-temp">Namlik:{{weather.main.humidity}}%</span>
             </div>
           </div>
           <div class="rain-info big-temp q-ml-lg q-mb-lg">
             Shamol tezligi:{{weather.wind.speed}}m/s
           </div>
        </div>
        <div class="col-11 q-mt-lg new-content ">
          <div class="q-ma-lg justify-center row items-center bit-content">
            <div class="row justify-around items-center " style="width:99%; height:100%">
              <div class="new-dey-tem new-day q-ml-md q-pr-md">31.02.2022</div>
              <div class=" new-icon q-ml-md " style="font-size:25px">O</div>
              <div class="new-dey-tem new-tem q-pl-md q-ml-md"><span>28ºC</span></div>
            </div>
          </div>
          <div class="q-ma-lg justify-center row items-center bit-content">
            <div class="row justify-around items-center " style="width:99%">
              <div class="new-dey-tem new-day q-ml-md q-pr-md">31.02.2022</div>
              <div class=" new-icon q-ml-md " style="font-size:25px">O</div>
              <div class="new-dey-tem new-tem q-pl-md q-ml-md"><span>28ºC</span></div>
            </div>
          </div>
          <div class="q-ma-lg justify-center row items-center bit-content">
            <div class="row justify-around items-center " style="width:99%; height:100%">
              <div class="new-dey-tem new-day q-ml-md q-pr-md">31.02.2022</div>
              <div class=" new-icon q-ml-md " style="font-size:25px">O</div>
              <div class="new-dey-tem new-tem q-pl-md q-ml-md"><span>28ºC</span></div>
            </div>
          </div>
          <div class="q-ma-lg justify-center row items-center bit-content">
            <div class="row justify-around items-center " style="width:99%; height:100%">
              <div class="new-dey-tem new-day q-ml-md q-pr-md">31.02.2022</div>
              <div class=" new-icon q-ml-md " style="font-size:25px">O</div>
              <div class="new-dey-tem new-tem q-pl-md q-ml-md"><span>28ºC</span></div>
            </div>
          </div>
          <div class="q-ma-lg justify-center row items-center bit-content">
            <div class="row justify-around items-center " style="width:99%; height:100%">
              <div class="new-dey-tem new-day q-ml-md q-pr-md">31.02.2022</div>
              <div class=" new-icon q-ml-md " style="font-size:25px">O</div>
              <div class="new-dey-tem new-tem q-pl-md q-ml-md"><span>28ºC</span></div>
            </div>
          </div>

        </div>
      </div>
    </div>
    <h4  style="position: relative;">{{weather}}</h4>
  </div>
</template>
<script>
export default {
  props:["weather"],

}
</script>
<style scoped>
  .big-temp{
    font-size: 24px;
    color: #FFFFFF;
  }
  .big-icon{
      width:75px ;
      height:75px;
      border-radius:50%;
      background: #C4C4C4;
  }
  .page{
    width: 100%;
    height: 100vh;
    background-image: url("../assets/rainautumn.png");
    background-repeat: no-repeat;
    background-size: cover;
    position: fixed;

  }
  .contanier-page{
    position: relative;
  }
  .content{
    background: rgba(107, 137, 183, 0.5);
    border-radius: 13px;
  }
  .new-day{
    border-right:2px solid rgba(255, 255, 255, 0.53);
  }
  .new-content{
    background: rgba(255, 255, 255, 0.53);
    border-radius: 22px;
  }
  .new-tem{
    border-left:2px solid rgba(255, 255, 255, 0.53);
  }
  .bit-content{
    background: rgba(69, 85, 191, 0.5);
    border-radius: 12px;
    height: 65px;
  }
  .new-dey-tem{
    font-size: 24px;
    line-height: 29px;
    color: #FFFFFF;
  }
  @media screen and ( min-width: 600px ) {
    .page{
      background-image: url("../assets/rainautunmcomp.png");
    }
    .big-icon{
      width:100px ;
      height:100px;
    }
    .content{
      background: rgba(4, 54, 169, 0.1);
    }
    .big-temp{
      font-size: 32px;
    }
    .new-content{
      width: 70%;
    }
    .temp-info{
      margin-left: 26%;
    }
    .rain-info{
      text-align: center;
      font-size: 30px;
    }
    .bit-content{
      height: 80px;
    }
    .new-dey-tem{
      font-size: 28px;
    }
  }
  @media screen and ( max-width: 360px ) {
    .big-temp{
      font-size: 22px;
    }
    .new-dey-tem{
      font-size: 20px;
    }
    .new-icon{
      margin: 0%;
      padding-left: 10px;
    }
  }
</style>


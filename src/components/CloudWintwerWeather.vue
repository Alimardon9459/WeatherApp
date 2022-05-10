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
    width:70px ;
    height:70px;
    border-radius:50%;
    background: #C4C4C4;
  }
  .page{
    width: 100%;
    height: 100vh;
    background-image: url("../assets/cloudwinter.png");
    background-repeat: no-repeat;
    background-size: cover;
    position: fixed;

  }
  .contanier-page{
    position: relative;
  }
  .content{
    background: rgba(124, 144, 168, 0.36);
    border-radius: 13px;
  }
  .new-day{
    border-right:2px solid rgb(255, 255, 255);
  }
  .new-content{
    background: rgba(235, 191, 195, 0.65);
    border-radius: 22px;
  }
  .new-tem{
    border-left:2px solid rgb(255, 255, 255)
  }
  .bit-content{
    background: rgba(23, 35, 41, 0.3);
    border-radius: 12px;
    height: 65px;
  }
  .new-dey-tem{
    font-size: 24px;
    line-height: 29px;
    color: #ffffff;
  }
  @media screen and ( min-width: 600px ) {
    .page{
      background-image: url("../assets/cloudwintercomp.png");
    }
    .big-icon{
      width:100px ;
      height:100px;
      border-radius:50%;
      background: #C4C4C4;
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

<template>
  <div class="MainBody">
    <section class="sec-padding">
      <div
        class="front_bkg"
        style="width:100%; height:100%;position: absolute;top: 0; overflow:hidden;opacity:0.8; background-image:url('images/bk.png')"
      ></div>
      <div class="container">
        <div class="row-custom m-1-1">
          <div
            class="col-custom w-2 relative"
            id="dutch"
            style="z-index: 1; background-image:url('images/group3-1/Layer 25 copy.png'); background-size: cover;"
          >
            <img class="item-dutch-money" src="images/group3-1/02.png" />
            <img class="item-dutch-hammer" src="images/group3-1/hammer.png" />
            <img class="item-dutch-bottom" src="images/group3-1/Layer-update2.png" />
            <div class="item-dutch-title">Dutch auction</div>
          </div>

          <div
            class="col-custom w-2 relative"
            id="crash"
            style="z-index: 1; background-image:url('images/group1-2/Layer 12.png'); background-size: cover;"
          >
            <img class="item-crash-point-1" src="images/group1-2/point.png" />
            <p class="item-crash-point-1-txt">9999.99x</p>
            <img class="item-crash-point-2" src="images/group1-2/point.png" />
            <p class="item-crash-point-2-txt">300.99x</p>
            <img class="item-crash-point-3" src="images/group1-2/point.png" />
            <p class="item-crash-point-3-txt">100.99x</p>
            <img class="item-crash-rocket" src="images/group1-2/rocket.png" />
            <div class="item-crash-title">Crash</div>
          </div>
        </div>

        <div class="row-custom m-1-1">
          <div
              class="col-custom w-2 relative"
              id = "poker"
              style="z-index: 1; background-image:url('images/group4-3/Layer 25.png'); background-size: cover;"
          >
            <img class="item-poker-ms" src="images/group4-3/Layer 26.png" />
            <img class="item-poker-pokers" src="images/group4-3/Layer 1.png" />
            <img class="item-poker-circle-core" src="images/group4-3/circle1.png" />
            <img class="item-poker-circle-border" src="images/group4-3/circle-border.png" />
            <img class="item-poker-coin" src="images/group4-3/coin.png" />
            <p class="item-poker-title">Online Poker</p>
          </div>

          <div class="col-custom w-2 d-flex" style="background: white; display: flex;">
            <div class="col-custom w-2 relative"
                 id = "baccarat"
                 style="z-index: 1; background-image:url('images/group8-4/Layer 16.png'); background-size: cover;"
            >
              <img class="item-baccarat" src="images/group8-4/Layer 17.png" />
              <div class="item-baccarat-title">Baccarat</div>
            </div>
            <div class="col-custom w-2 relative"
                 id = "penny"
                 style="z-index: 1; background-image:url('images/group9-5/bk.png'); background-size: cover;"
            >
              <img class="item-penny-hammer-bottom" src="images/group9-5/gold-hammer-bottom.png" />
              <img class="item-penny-hammer" src="images/group9-5/gold-hammer.png" />
              <img class="item-penny-cash" src="images/group9-5/cash.png" />
              <div class="item-penny-title">Penny auction</div>
            </div>
          </div>
        </div>

        <div class="row-custom m-1-1">
          <div class="col-custom w-2 d-flex" style="background: white; display: flex;">
            <div class="col-custom w-2 relative"
                 id = "roulette"
                 style="z-index: 1; background-image:url('images/group5-6/Layer 16 copy 2.png'); background-size: cover;"
            >
              <img class="item-roulette" src="images/group5-6/Layer 15.png" />
              <div class="item-roulette-title">Roulette </div>
            </div>

            <div class="col-custom w-2 relative"
                 id = "slot"
                 style="z-index: 1; background-image:url('images/group6-7/Layer 16.png'); background-size: cover;"
            >
              <img class="item-slot" src="images/group6-7/Layer.png" />
              <img class="item-slot-bell" src="images/group6-7/bell.png" />
              <div class="item-slot-title">Slot</div>
            </div>
          </div>

          <div class="col-custom w-2 relative"
               id = "black"
          >
            <img class="item-black" src="images/group7-8/Layer 21.png" />
            <div class="item-black-title">Black Jack</div>
          </div>
        </div>
      </div>
    </section>
    <div class="clearfix"></div>
    <section class="tab_sec">
      <div class="container">
        <div class="tab_city">
          <button class="tablinks active" onclick="openTab(event, 'tab1')">All</button>
          <button class="tablinks" onclick="openTab(event, 'tab2')">High Wins</button>
          <button class="tablinks" onclick="openTab(event, 'tab3')">Lucky Wins</button>
        </div>

        <div id="tab1" class="tabcontent" style="display: block;">
          <table id="customers">
            <tr>
              <th class="t_game">GAME</th>
              <th class="t_user m_invisible">USER</th>
              <th class="t_time m_invisible">TIME</th>
              <th class="wager m_invisible">WAGER</th>
              <th class="mult m_invisible">MULT</th>
              <th class="payout">PAYOUT</th>
            </tr>
            <tr v-for="(data,index) in  gameInfo" :key="index">
              <td class="t_game">{{data.t_game}}</td>
              <td class="t_user m_invisible">{{data.t_user}}</td>
              <td class="t_time m_invisible">{{data.t_time}}</td>
              <td class="wager m_invisible">
                {{data.wager}}
                <i class="icon"></i>
              </td>
              <td class="mult m_invisible">{{data.mult}}</td>
              <td class="payout">
                {{data.payout}}
                <i class="icon"></i>
              </td>
            </tr>
          </table>
        </div>

        <div id="tab2" class="tabcontent">
          <table id="customers">
            <tr>
              <th class="t_game">GAME</th>
              <th class="t_user m_invisible">USER</th>
              <th class="t_time m_invisible">TIME</th>
              <th class="wager m_invisible">WAGER</th>
              <th class="mult m_invisible">MULT</th>
              <th class="payout">PAYOUT</th>
            </tr>
            <tr v-for="(data,index) in  gameInfo" :key="index">
              <td class="t_game">{{data.t_game}}</td>
              <td class="t_user m_invisible">{{data.t_user}}</td>
              <td class="t_time m_invisible">{{data.t_time}}</td>
              <td class="wager m_invisible">
                {{data.wager}}
                <i class="icon"></i>
              </td>
              <td class="mult m_invisible">{{data.mult}}</td>
              <td class="payout">
                {{data.payout}}
                <i class="icon"></i>
              </td>
            </tr>
          </table>
        </div>

        <div id="tab3" class="tabcontent">
          <table id="customers">
            <tr>
              <th class="t_game">GAME</th>
              <th class="t_user m_invisible">USER</th>
              <th class="t_time m_invisible">TIME</th>
              <th class="wager m_invisible">WAGER</th>
              <th class="mult m_invisible">MULT</th>
              <th class="payout">PAYOUT</th>
            </tr>
            <tr v-for="(data,index) in  gameInfo" :key="index">
              <td class="t_game">{{data.t_game}}</td>
              <td class="t_user m_invisible">{{data.t_user}}</td>
              <td class="t_time m_invisible">{{data.t_time}}</td>
              <td class="wager m_invisible">
                {{data.wager}}
                <i class="icon"></i>
              </td>
              <td class="mult m_invisible">{{data.mult}}</td>
              <td class="payout">
                {{data.payout}}
                <i class="icon"></i>
              </td>
            </tr>
          </table>
        </div>
      </div>
    </section>
    <div class="clearfix"></div>
  </div>
</template>

<script>
export default {
  name: "home",
  props: {},
  data() {
    return {
      hammer: false,
      hammer_bottom: false,
      cash: false,
      active: false,
      gameInfo: [
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        },
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        },
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        },
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        },
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        },
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        },
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        },
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        },
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        },
        {
          t_game: "Aztec Magic Deluxe",
          t_user: "monday88",
          t_time: "9:18 PM",
          wager: "$1.5000",
          mult: "1.60x",
          payout: "$2.4000"
        }
      ]
    };
  },
  methods: {
    mouseOver() {
      this.active = !this.active;
    }
  }
};
</script>

<style>
/* 
 *  L A Y O U T
 */

.relative {
  position: relative;
}

.row-custom {
  display: flex;
  margin-top: 3rem;
  margin-bottom: 3rem;
}

.row-custom .col-custom {
  margin-left: 20px;
  margin-right: 20px;
  min-height: 200px;
  background-color: #aca;
}
.row-custom.m-1-1 .col-custom {
  margin: 0 10px;
}
/*.row-custom.m-1-2 .col-custom {*/
/*  margin: 0 10px;*/
/*}*/
.row-custom .col-custom:first-child {
  margin-left: 0;
}
.row-custom .col-custom:last-child {
  margin-right: 0;
}

.row-custom .col-custom.w-2 {
  width: 50%;
}
@media (max-width: 767px) {

  .row-custom { flex-wrap: wrap; margin: 0; max-width: 568px; margin: 0 auto; }
  .row-custom .col-custom.w-2 {
    width: 100%;
    margin: 3rem 0;
  }
}

/*.row-custom .col-custom.w-1 {*/
/*  width: 25%;*/
/*}*/

/*dutch*/
#dutch{
  border-radius: 5px;
}
#dutch .item-dutch-money {
  position: absolute;
  left: 39%;
  top: -6%;
  width: 53%;
  height: 92%;
  z-index: 2;
  transition: all 0.5s;
}

#dutch .item-dutch-bottom {
  position: absolute;
  left: 9%;
  top: -11%;
  width: 34%;
  height: 100%;
  z-index: 3;
  transition: all 0.5s;
  transform: translate(0, 0) rotate(0deg);
}

#dutch .item-dutch-hammer {
  position: absolute;
  left: 3%;
  top: -15%;
  width: 25%;
  height: 80%;
  z-index: 4;
  transition: all 0.5s;
  transform: translate(0, 0) rotate(0deg);
  transform-origin: 0 70%;
}
#dutch .item-dutch-title{
  position: absolute;
  top: 85%;
  left: 76%;

  font-size: 18px;
  font-weight: 700;
  color: white;
  font-family: cursive;
}
#crash .item-crash-title{
  position: absolute;
  top: 85%;
  left: 88%;
  font-size: 18px;
  font-family: cursive;
  font-weight: 700;
  color: white;
}
#poker .item-poker-title{
  position: absolute;
  top: 85%;
  left: 79%;
  font-size: 18px;
  font-family: cursive;
  font-weight: 700;
  color: white;
}
#dutch:hover .item-dutch-money {
  transform: scale(1.05);
}

#dutch:hover .item-dutch-bottom {
}

#dutch:hover .item-dutch-hammer {
  transform: translate(3%, 15%) rotate(-30deg);
}

/*crash*/
#crash{
  border-radius: 5px;
}
#crash .item-crash-point-1{
  position: absolute;
  z-index: 1;
  margin-top: 3%;
  margin-left: 56%;
}
#crash .item-crash-point-1-txt{
  position: absolute;
  z-index: 2;
  margin-top: 2%;
  margin-left: 41%;
  font-size: 18px;
  font-weight: 600;
  color: white;
}
#crash .item-crash-point-2{
  position: absolute;
  z-index: 1;
  margin-top: 12.4%;
  margin-left: 32%;
}
#crash .item-crash-point-2-txt{
  position: absolute;
  z-index: 2;
  margin-top: 8%;
  margin-left: 27%;
  font-size: 18px;
  font-weight: 600;
  color: white;
}
#crash .item-crash-point-3{
  position: absolute;
  z-index: 1;
  margin-top: 16%;
  margin-left: 16%;
}
#crash .item-crash-point-3-txt{
  position: absolute;
  z-index: 2;
  margin-top: 12%;
  margin-left: 11%;
  font-size: 18px;
  font-weight: 600;
  color: white;
}

#crash:hover .item-crash-point-2, #crash:hover .item-crash-point-3, #crash:hover .item-crash-point-1{
  -webkit-animation-name: hvr-pulse-shrink;
  animation-name: hvr-pulse-shrink;
  -webkit-animation-duration: 0.3s;
  animation-duration: 0.3s;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-direction: alternate;
  animation-direction: alternate;
}

#crash:hover .item-crash-point-1-txt, #crash:hover .item-crash-point-2-txt, #crash:hover .item-crash-point-3-txt{
  -webkit-animation-name: hvr-pulse-shrink;
  animation-name: hvr-pulse-shrink;
  -webkit-animation-duration: 0.3s;
  animation-duration: 0.3s;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-direction: alternate;
  animation-direction: alternate;
}

#crash .item-crash-rocket{
  position: absolute;
  z-index: 3;
  width: 61%;
  height: 90%;
  margin-left: 39%;
  margin-top: -1%;
  transition: all 0.5s;
  transform: translate(0px, 0px) rotate(-8deg);

}
#crash:hover .item-crash-rocket{
  position: absolute;
  z-index: 3;
  width: 61%;
  height: 90%;
  margin-left: 39%;
  margin-top: -1%;
  transform: translate(20px, -20px) rotate(-6deg);
}
/*poker*/
#poker{
  border-radius: 5px;
}
#poker .item-poker-ms{
  position: absolute;
  z-index: 1;
  width: 39%;
  height: 108.5%;
  margin-top: -3%;
  margin-left: 5%;
  transition: all 0.5s;
  transform: translate(0, 0) rotate(0deg);
}
#poker .item-poker-pokers{
  position: absolute;
  z-index: 2;
  width: 17%;
  height: 45%;
  margin-left: 24%;
  margin-top: 7%;
  transition: all 0.5s;

}
#poker .item-poker-circle-border{
  position: absolute;
  z-index: 0;
  /*width: 35%;*/
  height: 96%;
  width: auto;
  margin-left: 33.3%;
  top: 4%;
  -webkit-transition: all 0.5s;
  transition: all 0.5s;
}
#poker .item-poker-circle-core{
  position: absolute;
  z-index: 0;
  height: 68%;
  margin-left: 38.7%;
  top: 24%;
  -webkit-transition: all 0.5s;
  transition: all 8s;
}
#poker:hover .item-poker-circle-core{
  transform: translate(0px, 0px) rotate(720deg);
}
#poker:hover .item-poker-pokers{
  -webkit-transform: scale3d(1.2, 1.2, 1.5) rotate(-180deg);
}
#poker .item-poker-coin{
  position: absolute;
  z-index: 5;
  top: 10%;
  left: 60%;
}
#poker:hover .item-poker-coin{
  transform: translate(0px, 0px) rotateZ(45deg);
}

/*baccarat*/
#baccarat{
  border-radius: 5px;
}
#baccarat .item-baccarat{
  position: absolute;
  top: -5%;
  left: 20%;
  width: 63%;
  height: 90%;
}
#baccarat:hover .item-baccarat{
  -webkit-animation-name: hvr-pulse-shrink;
  animation-name: hvr-pulse-shrink;
  -webkit-animation-duration: 0.3s;
  animation-duration: 0.3s;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-direction: alternate;
  animation-direction: alternate;
}
#baccarat .item-baccarat-title{
  position: absolute;
  top: 85%;
  left: 69%;
  font-size: 18px;
  font-family: cursive;
  font-weight: 700;
  color: white;
}

/*penny*/
#penny{
  border-radius: 5px;
}
#penny .item-penny-hammer-bottom{
  position: absolute;
  width: 43%;
  height: 13%;
  top: 67%;
  left: 24%;
}
#penny .item-penny-hammer{
  position: absolute;
  width: 63%;
  height: 53%;
  top: 24%;
  left: 36%;
  z-index: 4;
  transition: all 0.5s;
  transform: translate(0, 0) rotate(0deg);
  transform-origin: 90% 40%;
}
#penny:hover .item-penny-hammer{
  transform: translate(5%, 5%) rotate(15deg);
}
#penny .item-penny-cash{
  position: absolute;
  top: -14%;
  left: 14%;
  width: 72%;
  height: 93%;
  z-index: 1;
  transition: all 0.5s;
  transform: translate(0, 0) rotate(0deg);
}
#penny:hover .item-penny-cash{
   transform: scale(0.9);
}
#penny .item-penny-title{
  position: absolute;
  top: 85%;
  left: 54%;
  font-size: 18px;
  font-family: cursive;
  font-weight: 700;
  color: white;
}

/*roulette*/
#roulette{
  border-radius: 5px;
}
#roulette .item-roulette{
  position: absolute;
  top: -11%;
  left: 19%;
  width: 66%;
  height: 100%;
}
#roulette:hover .item-roulette{
  -webkit-animation-name: hvr-pulse-shrink;
  animation-name: hvr-pulse-shrink;
  -webkit-animation-duration: 0.3s;
  animation-duration: 0.3s;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-direction: alternate;
  animation-direction: alternate;
}
#roulette .item-roulette-title{
  position: absolute;
  top: 85%;
  left: 70%;
  font-size: 18px;
  font-family: cursive;
  font-weight: 700;
  color: white;
}

/*slot*/
#slot{
  border-radius: 5px;
}
#slot .item-slot{
  position: absolute;
  top: 6%;
  left: 13%;
  width: 71%;
  height: 74%;
  transition: all 0.5s;
  transform: translate(0, 0) rotate(0deg);
}
#slot .item-slot-bell{
  position: absolute;
  width: 10%;
  height: 10%;
  top: 53%;
  left: 70%;
  z-index: 3;
  transition: all 0.5s;
  transform: translate(0, 0) rotate(0deg);
}
#slot:hover .item-slot-bell{
  -webkit-animation-name: hvr-wobble-bottom;
  animation-name: hvr-wobble-bottom;
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-timing-function: ease-in-out;
  animation-timing-function: ease-in-out;
  -webkit-animation-iteration-count: 3;
  animation-iteration-count: 3;
  transform: rotate(-2deg);
}
#slot .item-slot-title{
  position: absolute;
  top: 85%;
  left: 84%;
  font-size: 18px;
  font-family: cursive;
  font-weight: 700;
  color: white;
}

#slot:hover .item-slot{
  transform: rotate(3deg);
}
/*black*/
#black{
  border-radius: 5px;
}
#black .item-black{
  position: absolute;
  width: 100%;
  height: 113%;
  top: -13%;
}
#black .item-black-title{
  position: absolute;
  top: 85%;
  left: 82%;
  font-size: 18px;
  font-family: cursive;
  font-weight: 700;
  color: white;
  transition: all 0.5s;
  transform: translate(0, 0) rotate(0deg);
}
#black:hover .item-black{
  transform: scale(1.01);
}

/*title hover*/
#slot:hover .item-slot-title, #black:hover .item-black-title, #roulette:hover .item-roulette-title, #penny:hover .item-penny-title,
#baccarat:hover .item-baccarat-title, #poker:hover .item-poker-title, #crash:hover .item-crash-title, #dutch:hover .item-dutch-title{
  -webkit-animation-name: hvr-wobble-bottom;
  animation-name: hvr-wobble-bottom;
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-timing-function: ease-in-out;
  animation-timing-function: ease-in-out;
  -webkit-animation-iteration-count: 1;
  animation-iteration-count: 1;
}


@media only screen and (max-width: 1000px) {
  .m_invisible {
    display: none;
  }
  #customers tr {
    font-size: 15px;
  }
}
@media only screen and (max-width: 1200px) {
  #dutch .item-dutch-title {
    position: absolute;
    top: 85%;
    left: 72%;
    font-size: 18px;
    font-weight: 700;
    color: white;
    font-family: cursive;
  }
  #crash .item-crash-rocket {
    margin-left: 54%;
  }
  #crash:hover .item-crash-rocket {
    position: absolute;
    z-index: 3;
    width: 61%;
    height: 90%;
    margin-left: 54%;
    margin-top: -1%;
    transform: translate(8px, -10px) rotate(-4deg);
  }
  #crash .item-crash-point-3 {
    margin-top: 21%;
  }
  #crash .item-crash-point-3-txt {
    margin-top: 15%;
  }
  #crash .item-crash-point-2 {
    margin-top: 17.4%;
  }
  #crash .item-crash-point-2-txt {
    margin-top: 12%;
  }
  #crash .item-crash-point-1 {
    margin-top: 10%;
  }
  #crash .item-crash-point-1-txt {
    margin-top: 5%;
  }
  #crash .item-crash-rocket {
    margin-left: 53%;
    width: 58%;
    height: 74%;
    top: 10%;
  }
  #crash:hover .item-crash-rocket {
    position: absolute;
    z-index: 3;
    width: 64%;
    height: 75%;
    margin-left: 44%;
    margin-top: 6%;
    transform: translate(35px, -40px) rotate(-8deg);
  }
  #poker .item-poker-circle-border{
    /*width: 42%;*/
  }
  #poker .item-poker-title{
    left: 75%;
  }
  #poker .item-poker-circle-core {
    position: absolute;
    z-index: 0;
    height: 68%;
    margin-left: 39.9%;
    top: 24%;
    -webkit-transition: all 8s;
    transition: all 8s;
  }
  #baccarat .item-baccarat-title {
    left: 63%;
  }
  #penny .item-penny-title {
    left: 45%;
  }
  #black .item-black-title {
    left: 79%;
  }

}
@media only screen and (max-width: 990px) {
  #dutch .item-dutch-title {
    left: 64%;
  }
  #dutch .item-dutch-money {
    width: 59%;
  }
  #dutch .item-dutch-bottom {
    width: 41%;
    height: 98%;
    left: 5%;
  }
  #dutch .item-dutch-hammer {
    width: 26%;
    height: 71%;
    left: 2%;
    top: -9%;
  }
  #crash .item-crash-rocket {
    margin-left: 59%;
    width: 66%;
    height: 67%;
    top: 22%;
    transform: translate(0px, 0px) rotate(-14deg);
  }
  #crash:hover .item-crash-rocket {
    margin-left: 59%;
    width: 66%;
    height: 67%;
    top: 22%;
    transform: translate(15px, -30px) rotate(-14deg);
  }
  #crash .item-crash-title {
    left: 85%;
  }
  #crash .item-crash-point-1 {
    margin-top: 19%;
  }
  #crash .item-crash-point-1-txt {
    top: 11%;
    left: 9%;
    font-size: 16px;
  }
  #crash .item-crash-point-2 {
    margin-top: 25.4%;
  }
  #crash .item-crash-point-2-txt {
    top: 11%;
    left: 4%;
    font-size: 16px;
  }
  #crash .item-crash-point-3 {
    margin-top: 28%;
    margin-left: 17%;
  }
  #crash .item-crash-point-3-txt {
    margin-top: 21%;
    font-size: 16px;
    left: 4%;
  }
  #poker .item-poker-circle-border{
    /*width: 56%;*/
    /*left: -3%;*/
  }
  #poker .item-poker-title {
    left: 67%;
  }
  #poker .item-poker-circle-core{
    margin-left: 42%;
  }
  #baccarat .item-baccarat-title {
    left: 51%;
  }
  #penny .item-penny-title {
    left: 27%;
  }
  #black .item-black-title {
    left: 71%;
  }
  #slot .item-slot-title {
    left: 76%;
  }
  #roulette .item-roulette-title {
    left: 53%;
  }


}
@media only screen and (max-width: 767px) {
  #dutch .item-dutch-title {
    left: 76%;
  }
  #dutch .item-dutch-money {
    width: 53%;
  }
  #dutch .item-dutch-bottom {
    left: 9%;
    top: -11%;
    width: 34%;
    height: 100%;
  }
  #dutch .item-dutch-hammer {
    width: 26%;
    height: 71%;
    left: 2%;
    top: -9%;
  }
  #crash .item-crash-rocket{

    z-index: 3;
    width: 61%;
    height: 88%;
    margin-left: 39%;
    margin-top: -9%;
    transition: all 0.5s;
    transform: translate(0px, 0px) rotate(-8deg);

  }
  #crash:hover .item-crash-rocket{
    z-index: 3;
    width: 61%;
    height: 88%;
    margin-left: 39%;
    margin-top: -9%;
    transition: all 0.5s;
    transform: translate(10px, -10px) rotate(-11deg);
  }
  #crash .item-crash-title {
    left: 90%;
  }
  #crash .item-crash-point-3 {
    margin-top: 16%;
    margin-left: 17%;
  }
  #crash .item-crash-point-3-txt {
    margin-top: 12%;
    font-size: 16px;
    left: 0;
  }
  #crash .item-crash-point-2 {
    margin-top: 12.4%;
  }
  #crash .item-crash-point-1 {
    margin-top: 19%;
  }
  #crash .item-crash-point-2-txt {
    top: -11%;
    left: 2%;
    font-size: 16px;
  }
  #crash .item-crash-point-1 {
    margin-top: 3%;
  }

  #crash .item-crash-point-1-txt{
    top: -16%;
  }
  #poker .item-poker-circle-border {
    /*width: 35%;*/
    /*left: 0;*/
  }
  #poker .item-poker-title {
    left: 80%;
  }
  #poker .item-poker-circle-core {
    margin-left: 38.9%;
  }
  #penny{
    margin-left: 5%;
  }
  #slot{
    margin-left: 5%;
  }
  #baccarat .item-baccarat-title {
    left: 69%;
  }
  #penny .item-penny-title {
    left: 54%;
  }
  #roulette .item-roulette-title {
    left: 71%;
  }
  #slot .item-slot-title {
    left: 85%;
  }
  #black .item-black-title {
    left: 82%;
  }
  #poker .item-poker-title {
    left: 77%;
  }
  #penny .item-penny-title {
    left: 49%;
  }
  #black .item-black-title {
    left: 80%;
  }
  #roulette .item-roulette-title {
    left: 68%;
  }
  #slot .item-slot-title {
    left: 84%;
  }
  #penny .item-penny-title {
    left: 48%;
  }
}
@media only screen and (max-width: 584px) {

  #penny .item-penny-title {
    left: 49%;
  }

}
@media only screen and (max-width: 546px) {
  #dutch .item-dutch-title {
    left: 75%;
  }
  #poker .item-poker-title {
    left: 78%;
  }
  #penny .item-penny-title {
    left: 52%;
  }

}

@media only screen and (max-width: 528px) {
  #dutch .item-dutch-title {
    left: 73%;
  }

}

@media only screen and (max-width: 375px) {
  #dutch .item-dutch-title {
    left: 62%;
  }
#crash .item-crash-rocket{
  z-index: 3;
  width: 64%;
  height: 69%;
  margin-left: 50%;
  margin-top: 7%;
  -webkit-transition: all 0.5s;
  transition: all 0.5s;
  -webkit-transform: translate(0px, 0px) rotate(-8deg);
  transform: translate(0px, 0px) rotate(-11deg);
}
  #crash:hover .item-crash-rocket{
    z-index: 3;
    width: 64%;
    height: 69%;
    margin-left: 50%;
    margin-top: 7%;
    -webkit-transition: all 0.5s;
    transition: all 0.5s;
    -webkit-transform: translate(0px, 0px) rotate(-8deg);
    transform: translate(6px, -10px) rotate(-11deg);
  }
  #crash .item-crash-point-1 {
    margin-top: 15%;
    left: 14%;
  }
  #crash .item-crash-point-1-txt {
    top: 5%;
    left: 18%;
  }
  #crash .item-crash-point-2 {
    margin-top: 23.4%;
    left: 13%;
  }
  #crash .item-crash-point-2-txt {
    top: 5%;
    left: 10%;
    font-size: 16px;
  }
  #crash .item-crash-point-3 {
    margin-top: 28%;
    margin-left: 22%;
  }
  #crash .item-crash-point-3-txt {
    margin-top: 21%;
    font-size: 16px;
    left: 18px;
  }
  #crash .item-crash-title {
    left: 84%;
  }
  #poker .item-poker-circle-core {
    position: absolute;
    z-index: 0;
    height: 68%;
    margin-left: 42.7%;
    top: 24%;
    -webkit-transition: all 8s;
    transition: all 8s;
  }
  #poker .item-poker-title {
    left: 68%;
  }
  #baccarat .item-baccarat-title {
    left: 51%;
  }
  #penny .item-penny-title {
    left: 27%;
  }
  #roulette .item-roulette-title {
    left: 54%;
  }
  #slot .item-slot-title {
    left: 77%;
  }
  #black .item-black-title {
    left: 71%;
  }


}
</style>

<template>
  <v-app dark>
    <v-content>

      <!-- Bike image-->
      <section>
        <v-parallax src="https://images.pexels.com/photos/258045/pexels-photo-258045.jpeg?cs=srgb&dl=bicycle-cloud-clouds-258045.jpg&fm=jpg" height="600">
          <v-toolbar id="toolbar" dark flat v-bind:class="{ transparent: toolbarIsTransparent }">
            <v-toolbar-title class="titlev">HAYDEN</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-items class="hidden-sm-and-down">
              <v-layout>
              <v-btn class="titlev" :flat="flat1">About</v-btn>
              <v-btn class="titlev" flat>Services</v-btn>
              <v-btn class="titlev" flat>Resume</v-btn>
              </v-layout>
            </v-toolbar-items>
          </v-toolbar>
          <v-layout
            column
            align-center
            justify-center
            class="white--text"
          >
            <h1 class="heads">Hayden Hoffman</h1>
            <h1 class="heads2">Life Made Ridiculously Simple</h1>
            <canvas id="dontaskwhythiscanvasishere" width="100" height="100">
            </canvas>
            <v-btn
              fab
              dark
              small
              elevation-10
              color="black">
              <v-icon>close</v-icon>
            </v-btn>

          </v-layout>
        </v-parallax>
      </section>
      <!-- timeline -->
      <section>
        <v-layout
          column
          wrap
          class="my-5"
          align-center
        >
          <v-flex xs12 sm4 class="my-3">
            <div class="text-xs-center">
              <h2 class="heads3">About Me</h2>
            </div>
          </v-flex>
          <v-avatar
            :tile="tile"
            :size="'150px'"
            color="grey lighten-4"
            class="elevation-20"
          >
            <img id="profile" :src="'https://i.imgur.com/KYZJmsq.jpg?1'">
          </v-avatar>
          <v-flex xs12>
            <v-container grid-list-xs>
              <v-layout row wrap align-center>
                <v-timeline id="timeline">
                  <v-timeline-item
                    v-for="n in 2"
                    :key="n"
                    color="red lighten-3"
                    medium
                  >
                    <v-layout>
                      <v-flex xs12>
                        <v-card :color="items.color[n - 1]">
                          <v-parallax
                            height="200"
                            src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
                          ></v-parallax>
                          <v-card-text>
                          <h3 class="headline">{{items.headlines[n - 1]}}</h3>
                          <div>{{items.stories[n - 1]}}</div>
                          </v-card-text>
                        </v-card>
                      </v-flex>
                    </v-layout>
                    <canvas slot="opposite" id="game" width="300" height="400"></canvas>
                  </v-timeline-item>
                </v-timeline>
              </v-layout>
            </v-container>
          </v-flex>
        </v-layout>
      </section>
      <!-- web development has never been easier -->
      <section>
        <v-parallax src="https://images.pexels.com/photos/256502/pexels-photo-256502.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" height="380">
          <v-toolbar id="toolbar" dark flat v-bind:class="{ transparent: toolbarIsTransparent }">
            <v-toolbar-title class="titlev">HAYDEN</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-items class="hidden-sm-and-down">
              <v-btn class="titlev" flat>About</v-btn>
              <v-btn class="titlev" flat>Services</v-btn>
              <v-btn class="titlev" flat>Resume</v-btn>
            </v-toolbar-items>
          </v-toolbar>
          <v-layout column align-center justify-center>
            <div class="headline white--text mb-3 text-xs-center">Web development has never been easier</div>
            <em>Kick-start your application today</em>
            <v-btn
              class="blue lighten-2 mt-5"
              dark
              large
              href="/pre-made-themes"
            >
              Get Started
            </v-btn>
          </v-layout>
        </v-parallax>
      </section>

      <section>
        <v-container grid-list-xl>
          <v-layout row wrap justify-center class="my-5">
            <v-flex xs12 sm4>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Company info</div>
                </v-card-title>
                <v-card-text>
                  Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                  Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                  Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.
                </v-card-text>
              </v-card>
            </v-flex>
            <v-flex xs12 sm4 offset-sm1>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Contact us</div>
                </v-card-title>
                <v-card-text>
                  Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                </v-card-text>
                <v-list class="transparent">
                  <v-list-tile>
                    <v-list-tile-action>
                      <v-icon class="blue--text text--lighten-2">phone</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                      <v-list-tile-title>777-867-5309</v-list-tile-title>
                    </v-list-tile-content>
                  </v-list-tile>
                  <v-list-tile>
                    <v-list-tile-action>
                      <v-icon class="blue--text text--lighten-2">place</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                      <v-list-tile-title>Chicago, US</v-list-tile-title>
                    </v-list-tile-content>
                  </v-list-tile>
                  <v-list-tile>
                    <v-list-tile-action>
                      <v-icon class="blue--text text--lighten-2">email</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                      <v-list-tile-title>john@vuetifyjs.com</v-list-tile-title>
                    </v-list-tile-content>
                  </v-list-tile>
                </v-list>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </section>

      <v-footer class="blue darken-2">
        <v-layout row wrap align-center>
          <v-flex xs12>
            <div class="white--text ml-3">
              Made with
              <v-icon class="red--text">favorite</v-icon>
              by <a class="white--text" href="https://vuetifyjs.com" target="_blank">Vuetify</a>
              and <a class="white--text" href="https://github.com/vwxyzjn">Costa Huang</a>
            </div>
          </v-flex>
        </v-layout>
      </v-footer>
    </v-content>
  </v-app>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import Vuesax from 'vuesax'
import 'vuesax/dist/vuesax.css'
export default {
  data:()=>({
    me: this,
    flat1: true,
    flat2: true,
    flat3: true,
    colorAlert:'primary',
    titleAlert:'Alert',
    activeAlert:false,
    valueInput:'',
    toolbarIsTransparent: true,
    story1: "yo",
    story2: "hey",
    story3: "wassup",
    story4: "yeet",
    items: {
      dir: [
        'right',
        'left',
        'right',
        'left'
      ],
      color: [
        'purple lighten-2',
        'green',
        'blue'
      ],
      stories: [
      'Yo so this is a story all about how my life got flip-turned upside down. And I had a lotta image with a bottle of jack, touch my knees and give me scotch, that\'s the way to be back.',
      'Yo so this is a story all about how my life got flip-turned upside down. And I had a lotta image with a bottle of jack, touch my knees and give me scotch, that\'s the way to be back.',
      'Yo so this is a story all about how my life got flip-turned upside down. And I had a lotta image with a bottle of jack, touch my knees and give me scotch, that\'s the way to be back.',
      'Yo so this is a story all about how my life got flip-turned upside down. And I had a lotta image with a bottle of jack, touch my knees and give me scotch, that\'s the way to be back.'
    ], headlines: [
      'hey',
        'wassup',
        'yo',
        'beaut'
      ]},
    maps: null,
    score: 0
  }),
  created () {

  },
  mounted () {
    const aos = require('aos');
    aos.init();
    const game = document.getElementById('game');
    const context = game.getContext('2d');
    //const context = this.context;
    (function() {
      var ball, paddle, A_I,
        speedX = 2,//This is a constant
        speedY = 0, //This will change
        game = document.getElementById('game'),
        ctx = game.getContext('2d'),
        score = [0, 0],
        center = [game.width / 2, game.height / 2 - 190],
        fps = 75;

      function drawBox(x, y, size, size2) {
        ctx.fillStyle = 'black';
        ctx.fillRect(x, y, size, size2);
      }

      function handleKeys(e) {
        var keys = [37, 39]; //in the format wasd, but with arrow keys
        for (var i = 0; i < keys.length; i++) {
          if (e.keyCode === keys[i]) {
            switch(i) {
              case 0:
                paddle.dir = "up";
                break;
              case 1:
                paddle.dir = "down";
                break;
            }

          }
          else continue;
        }
        return true;
      }

      function bounce(ai, paddle, obj) {
//This allows the ball to bounce
        obj.dir.y = (((obj.dir.y === "down" && obj.curPos[1] >= game.height - 25) ? "up" : null) ||
          ((obj.dir.y === "up" && obj.curPos[1] <= 0) ? "down" : null) || obj.dir.y);
        if ((obj.dir.x === "left" || obj.dir.y === "center") && obj.curPos[0] <= ai.curPos[0] + 25) {
          (obj.curPos[1] <= ai.curPos[1] && obj.curPos[1] >= ai.curPos[1] - 25)
            ? (speedY += 1, obj.dir.y = "up", obj.dir.x = "right") : null;
          (obj.curPos[1] <= ai.curPos[1] + 25 && obj.curPos[1] >= ai.curPos[1])
            ? obj.dir.x = "right" : null;
          (obj.curPos[1] <= ai.curPos[1] + 50 && obj.curPos[1] >= ai.curPos[1] + 25)
            ? (obj.dir.x = "right", speedY += 1, obj.dir.y = "down") : null;
        }
        // Checks for x coordinates, then for the y coordinates
        else if (obj.dir.x === "right" && obj.curPos[0] >= paddle.curPos[0] - 25) {
          (obj.curPos[1] <= paddle.curPos[1] + 0 && obj.curPos[1] >= paddle.curPos[1] - 25)
            ? (speedY += 1, obj.dir.y = "up", obj.dir.x = "left") : null;
          (obj.curPos[1] <= paddle.curPos[1] + 25 && obj.curPos[1] >= paddle.curPos[1])
            ? (speedY += 1, obj.dir.y = "up", obj.dir.x = "left") : null;
          (obj.curPos[1] <= paddle.curPos[1] + 50 && obj.curPos[1] >= paddle.curPos[1] + 25)
            ? obj.dir.x = "left" : null;
          (obj.curPos[1] <= paddle.curPos[1] + 75 && obj.curPos[1] >= paddle.curPos[1] + 50)
            ? (speedY += 1, obj.dir.y = "down", obj.dir.x = "left") : null;
        }

      }

      function AI(ai, obj) {
        var buffer = 10;
        var y = 1;
        if (ai.curPos[y] + 25 - buffer > obj.curPos[y]) {
          ai.dir = "up";
        } else if (ai.curPos[y] + 25 + buffer < obj.curPos[y]) {
          ai.dir = "down";
        } else {
          ai.dir = "center";
        }
      }
      function move(obj, pad, ai) {
//This also handles paddle and AI movement
        var x = 0, y = 1;
        var handler = [obj, pad, ai];
        for (var i = 0; i < 3; i++) {
          switch(handler[i].dir.y || handler[i].dir) {
            case "up":
              handler[i].curPos[y] -= (i === 0) ? speedY : 15;
              if (i !== 0 && handler[i].curPos[y] < 25) {
                while(handler[i].curPos[y] < 25) handler[i].curPos[y]++;
              }
              break;
            case "down":
              handler[i].curPos[y] += (i === 0) ? speedY : 15;
              if (i !== 0 && handler[i].curPos[y] > game.height - 75) {
                while(handler[i].curPos[y] > game.height - 75) handler[i].curPos[y]--;
              }
              break;
            case "center":
              break;
          }
        }
        obj.curPos[0] += (obj.dir.x === "left") ? -speedX : speedX;
      }
      function getScore(obj) {
          return obj.curPos[0] > 300;
      }
        /*((obj.curPos[0] <= 0) ? (alert("player 1 scored"), funcs.a0()) : null) ||
        ((obj.curPos[0] >= game.width) ? (alert("Computer scored"), funcs.a0()): null);
        if (score[0] - score[1] >= 2 && score[0] >= 7) {
          alert("Player 1 wins");
          location.reload();
        }
        else if (score[1] - score[0] >= 2 && score[1] >= 7) {
          alert("Computer wins");
          location.reload();
        }
      }*/

        ball = {
          curPos: [center[0], center[1]],
          dir: {x: "right", y: "center"}
        };

        A_I = {
          curPos: [25, center[1] + 25],
          dir: "center"
        };

        paddle = {  //The paddle that the user will control
          curPos: [game.width - 25, center[1] + 25],
          dir: "center"
        };
        function update() {  //Runs all of the code functions simultaneously
          ctx.clearRect(0, 0, game.width, game.height);
          drawBox(ball.curPos[0], ball.curPos[1], 25, 25);
          drawBox(paddle.curPos[0], paddle.curPos[1], 25, 75);
          drawBox(A_I.curPos[0], A_I.curPos[1], 25, 75);
          bounce(A_I, paddle, ball);
          move(ball, paddle, A_I);
          AI(A_I, ball);
          if (speedY > 10) speedY = 10;
          window.addEventListener("keydown", handleKeys);
          window.addEventListener("keyup", function (e) {
            if (handleKeys(e, true)) paddle.dir = "center";
          });
        }

        setInterval(update, 1000 / fps); //This will run all of the code until said time
      })();
  },
  components: {
    Logo,
    VuetifyLogo,
    Vuesax
  },
  methods: {

  }
}
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css?family=Cabin+Sketch|Permanent+Marker|Titillium+Web|Unica+One');
  @import url(https://fonts.googleapis.com/css?family=Khula:700);
  #parallax {
    height: 30px;
  }
  #game {

  }
  #headline {
    font-family: 'Permanent Marker', cursive;
    -webkit-text-stroke-width: 0.002px;
    -webkit-text-stroke-color: black;
    font-size: 40px;
  }
  .heads4 {
    font-family: 'Titillium Web', cursive;
    font-size: 17px;
  }
  .heads3 {
    font-family: 'Permanent Marker', cursive;
    -webkit-text-stroke-width: 0.002px;
    -webkit-text-stroke-color: black;
    font-size: 40px;
  }
  .titlev {
    font-size: 15px;
    font-family: 'Permanent Marker', cursive;
    -webkit-text-stroke-width: 1px;
    -webkit-text-stroke-color: black;
  }
  #profile {
    width: 110%;
  }
#toolbar {
  position: fixed;
  top: 0%;
}
#timeline {
  width: 70%;
  left: 15%;
}
.heads {
  font-family: 'Permanent Marker', cursive;
  -webkit-text-stroke-width: 0.002px;
  -webkit-text-stroke-color: black;
  font-size: 105px;
}
  .heads2{
    font-family: 'Unica One', cursive;
    -webkit-text-stroke-width: 0.002px;
    -webkit-text-stroke-color: black;
    font-size: 60px;
  }
  .console-container {

    font-family:Khula;
    font-size:4em;
    text-align:center;
    height:200px;
    width:600px;
    display:block;
    position:absolute;
    color:white;
    top:0;
    bottom:0;
    left:0;
    right:0;
    margin:auto;
  }
  .console-underscore {
    display:inline-block;
    position:relative;
    top:-0.14em;
    left:10px;
  }
  .overlay {
    z-index: 1;
    height: fit-content;
    width: fit-content;
    position: fixed;
    overflow: auto;
    top: 0px;
    left: 0px;
    background: rgba(0, 0, 0, 0.7); /*can be anything, of course*/
  }
</style>

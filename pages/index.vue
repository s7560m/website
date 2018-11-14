<template>
  <v-app dark>
    <v-content>


      <section>
        <v-parallax src="https://images.pexels.com/photos/258045/pexels-photo-258045.jpeg?cs=srgb&dl=bicycle-cloud-clouds-258045.jpg&fm=jpg" height="600">
          <v-toolbar id="toolbar" dark flat v-bind:class="{ transparent: toolbarIsTransparent }">
            <v-toolbar-title class="titlev">HAYDEN</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-items class="hidden-sm-and-down">
              <v-btn class="titlev" flat>About</v-btn>
              <v-btn class="titlev" flat>Services</v-btn>
              <v-btn class="titlev" flat>Resume</v-btn>
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
                    v-for="n in 4"
                    :key="n"
                    color="red lighten-3"
                    medium
                  >
                    <v-card class="elevation-10">
                      <v-card-title class="headline">Lorem ipsum</v-card-title>
                      <v-card-text>
                        Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.
                      </v-card-text>
                    </v-card>
                  </v-timeline-item>
                </v-timeline>
              </v-layout>
            </v-container>
          </v-flex>
        </v-layout>
      </section>

      <section>
        <v-parallax src="assets/section.jpg" height="380">

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
    colorAlert:'primary',
    titleAlert:'Alert',
    activeAlert:false,
    valueInput:'',
    toolbarIsTransparent: true,
  }),
  mounted () {
    window.addEventListener('scroll', function() {
      // Will
      this.toolbarIsTransparent = !(window.scrollY > 10);
      console.log("yeah");
    })
  },
  updated () {
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
  font-size: 110px;
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

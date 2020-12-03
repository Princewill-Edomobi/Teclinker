<template>
  <v-app>
    <v-app-bar app color="teal lighten-1" height="100">
      <v-avatar class="mr-3" color="grey lighten-5" size="70">
        <v-img contain max-height="70%" src="../assets/logo.png"></v-img>
      </v-avatar>

      <v-toolbar-title class="font-weight-black teal--text text--darken-4 headline">
        P<span class="subtitle-1 font-weight-black">G</span>A A<span
          class="subtitle-1 font-weight-black"
          >DVISORY</span
        >
      </v-toolbar-title>
      <v-spacer class="hidden-sm-and-down"></v-spacer>
      <v-btn text class="hidden-sm-and-down  teal--text text--darken-4 " @click="$vuetify.goTo('#the-what')">THE WHAT</v-btn>
      <v-btn text class="hidden-sm-and-down  teal--text text--darken-4 " @click="$vuetify.goTo('#the-how')">THE HOW</v-btn>
      <v-btn text class="hidden-sm-and-down  teal--text text--darken-4 " @click="$vuetify.goTo('#contact')">CONTACT US</v-btn>
    </v-app-bar>

    <v-content>
      <section id="hero">
        <v-row no-gutters>
          <v-img
            :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
            src="https://images.unsplash.com/photo-1487017159836-4e23ece2e4cf?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1951&q=80"
          >
            <v-theme-provider dark>
              <v-container fill-height>
                <v-row
                  align="center"
                  class="white--text mx-auto"
                  justify="center"
                >
                  <v-col class="white--text text-center" cols="12" tag="h1">
                    <span
                      :class="[
                        $vuetify.breakpoint.smAndDown
                          ? 'display-1'
                          : 'display-2'
                      ]"
                      class="font-weight-light"
                    >
                      WELCOME TO
                    </span>

                    <br />

                    <span
                      :class="[
                        $vuetify.breakpoint.smAndDown
                          ? 'display-3'
                          : 'display-4'
                      ]"
                      class="font-weight-black"
                    >
                      PGA ADVISORY
                    </span>

                    <br />

                    <span
                      :class="[
                        $vuetify.breakpoint.smAndDown ? 'title' : 'headline'
                      ]"
                      class="font-italic"
                    >
                      'Weaving Technology into Business Models'
                    </span>
                  </v-col>

                  <v-btn
                    class="align-self-end"
                    fab
                    outlined
                    @click="$vuetify.goTo('#about-me')"
                  >
                    <v-icon>mdi-chevron-double-down</v-icon>
                  </v-btn>
                </v-row>
              </v-container>
            </v-theme-provider>
          </v-img>
        </v-row>
      </section>

      <section id="about-me">
        <div class="py-12"></div>

        <v-container class="text-center">
          <h2 class="display-2 font-weight-bold mb-3">ABOUT ME</h2>

          <v-responsive class="mx-auto mb-8" width="56">
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-responsive
            class="mx-auto title font-weight-light mb-8"
            max-width="720"
          >
            Morbi mattis ullamcorper velit. Donec orci lectus, aliquam ut,
            faucibus non, euismod id, nulla. Fusce convallis metus id felis
            luctus adipiscing. Aenean massa. Vestibulum purus quam, scelerisque
            ut, mollis sed, nonummy id, metus. Nulla consequat massa quis enim.
            Praesent venenatis metus at tortor pulvinar varius. Donec venenatis
            vulputate lorem. Phasellus accumsan cursus velit. Pellentesque ut
            neque.
          </v-responsive>

          <v-avatar class="elevation-12 mb-12" size="128">
            <v-img src="../assets/profile.jpg"></v-img>
          </v-avatar>

          <div></div>

          <v-btn
            color="grey"
            href="https://www.linkedin.com/in/gordon%2Danani%2D57521386/"
            outlined
            large
          >
            <span class="grey--text text--darken-1 font-weight-bold">
              LINKED IN
            </span>
          </v-btn>
        </v-container>

        <div class="py-12"></div>
      </section>

      <section id="the-what" class="grey lighten-3">
        <div class="py-12"></div>

        <v-container class="text-center">
          <h2 class="display-2 font-weight-bold mb-3">WHAT WE DO</h2>

          <v-responsive class="mx-auto mb-12" width="56">
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-row>
            <v-col
              v-for="({ icon, title, text }, i) in theWhat"
              :key="i"
              cols="12"
              md="4"
            >
              <v-card class="py-12 px-4" color="grey lighten-5" flat>
                <v-theme-provider dark>
                  <div>
                    <v-avatar color="teal lighten-2 " size="88">
                      <v-icon large v-text="icon"></v-icon>
                    </v-avatar>
                  </div>
                </v-theme-provider>

                <v-card-title
                  class="justify-center font-weight-black text-uppercase"
                  v-text="title"
                ></v-card-title>

                <v-card-text class="subtitle-1" v-text="text"> </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>

        <div class="py-12"></div>
      </section>

      <section id="stats">
        <v-parallax
          :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
          src="https://images.unsplash.com/photo-1510915228340-29c85a43dcfe?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80"
        >
          <v-container fill-height>
            <v-row class="mx-auto">
              <v-col
                v-for="[value, title] of stats"
                :key="title"
                cols="12"
                md="3"
              >
                <div class="text-center">
                  <div
                    class="display-3 font-weight-black mb-4"
                    v-text="value"
                  ></div>

                  <div
                    class="title font-weight-regular text-uppercase"
                    v-text="title"
                  ></div>
                </div>
              </v-col>
            </v-row>
          </v-container>
        </v-parallax>
      </section>

      <section id="the-how">
        <div class="py-12"></div>

        <v-container>
          <h2
            class="display-2 font-weight-bold mb-3 text-uppercase text-center"
          >
            HOW WE DO IT
          </h2>

          <v-responsive class="mx-auto mb-12" width="56">
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-row>
            <v-col
              v-for="({ src, text, title }, i) in theHow"
              :key="i"
              cols="12"
              md="3"
            >
              <v-img
                :src="src"
                class="mb-4"
                height="275"
                max-width="100%"
              ></v-img>

              <h3
                class="font-weight-black mb-4 text-uppercase"
                v-text="title"
              ></h3>

              <div class="title font-weight-light mb-5" v-text="text"></div>

            </v-col>
          </v-row>
        </v-container>

        <div class="py-12"></div>
      </section>

      <v-sheet id="contact" color="teal lighten-1" dark tag="section" tile>
        <div class="py-12"></div>

        <v-container>
          <h2
            class="display-2 font-weight-bold mb-3 text-uppercase text-center"
          >
            Contact us
          </h2>

          <v-responsive class="mx-auto mb-12" width="56">
            <v-divider class="mb-1"></v-divider>

            <v-divider></v-divider>
          </v-responsive>

          <v-theme-provider light>
            <v-row>
              <v-col cols="12">
                <v-text-field flat label="Name*" v-model="contact.name" solo></v-text-field>
              </v-col>

              <v-col cols="12">
                <v-text-field flat label="Email*" v-model="contact.email"  solo></v-text-field>
              </v-col>

              <v-col cols="12">
                <v-text-field flat label="Subject*" v-model="contact.subject" solo></v-text-field>
              </v-col>

              <v-col cols="12">
                <v-textarea flat label="Message*" v-model="contact.message" solo></v-textarea>
              </v-col>

              <v-col class="mx-auto" cols="auto">
                <v-btn color="teal darken-4 white--text" @click="submit()" x-large>
                  Submit
                </v-btn>
              </v-col>
            </v-row>
            
          </v-theme-provider>
        </v-container>

        <div class="py-12"></div>
      </v-sheet>
    </v-content>

    <v-footer class="justify-center" color="#292929" height="100">
      <div
        class="title font-weight-light grey--text text--lighten-1 text-center"
      >
        &copy; {{ new Date().getFullYear() }} — PGA ADVISORY, LLC — Philip Gordon Anani
      </div>
    </v-footer>
  </v-app>
</template>
<script>
export default {
  name: "home",
  components: {},
  data() {
    return {
      theHow: [
        {
          src:
            "https://images.unsplash.com/photo-1423784346385-c1d4dac9893a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80",
          title: "Understanding your vision",
          text:
            "By understanding the problems your business aims to solve. we are able to relate to the vision and goals."
        },
        {
          src:
            "https://images.unsplash.com/photo-1475938476802-32a7e851dad1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80",
          title: "Evaluating your strategy",
          text:
            "Evaluating your approach towards achieveing this vision and goals."
        },
        {
          src:
            "https://images.unsplash.com/photo-1416339442236-8ceb164046f8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1892&q=80",
          title: "Identifying Technological enhamcement",
          text:
            "Development ideas on how technology can turbo charge your business."
        },
        {
          src:
            "https://images.unsplash.com/photo-1416339442236-8ceb164046f8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1892&q=80",
          title: "Building your technology",
          text:
            "We have a team of professional developers equipped to building your technological future."
        }
      ],
      theWhat: [
        {
          icon: "mdi-account-group-outline",
          title: "Evaluation",
          text:
            "Evaluate effective technological structures from your Business Model."
        },
        {
          icon: "mdi-cloud-search-outline",
          title: "Finding Opportunties",
          text:
            "Finding Opportunities where technology can be weaved in."
        },
        {
          icon: "mdi-connection",
          title: "Connect Technology",
          text:
            "Our team of engineers then tailor the specfic technologies you require."
        }
      ],
      stats: [
        ["24k", "Companies"],
        ["330+", "Years"],
        ["1m", "Employees"],
        ["5m", "Technologies"]
      ],
      contact:{
        name: '',
        email: '',
        subject: '',
        message: ''
      }
    };
  },
  methods:{
    submit(){

    }
  }
};
</script>

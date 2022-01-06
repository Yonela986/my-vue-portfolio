<template>
  <div class="home">
    
    <v-img
      dark
      
      height="25rem"
      src="../assets/coverimage.jpg"
    >
      <v-layout fill-height align-center>
        <v-container>
          <v-row align="center" justify="center" class="white--text">
            <v-col cols="12">
              <div
                :class="{'display-2 font-weight-bold ': $vuetify.breakpoint.smAndUp, 'title font-weight-bold': $vuetify.breakpoint.smAndDown}"
              >Welcome to my page.</div>
              <div
                :class="{'headline': $vuetify.breakpoint.smAndUp, 'subtitle-1': $vuetify.breakpoint.smAndDown}"
              >I make applications.</div>
            </v-col>
          </v-row>
        </v-container>
      </v-layout>
    </v-img>
    <v-container class="mt-5">
      <v-layout wrap>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="about">About Me</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{aboutText}}</div>
          <div
            class="body-1 mt-3"
          ></div>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12>
          <div class="display-1 font-weight-bold" id="portfolio">My Work</div>
        </v-flex>
        <v-flex xs12 class="mt-5">
          <v-layout wrap>
            <template v-for="(app, i) in apps">
              <v-flex :key="i" xs12 sm6 md4>
                <portfolio-app :app="app" />
              </v-flex>
            </template>
          </v-layout>
        </v-flex>
      </v-layout>
      <v-layout wrap my-5>
        <v-flex xs12 mb-5>
          <div class="display-1 font-weight-bold" id="contact">Send Me a Message:</div>
        </v-flex>
        <template v-for="(contact, i) in contactLinks">
          <v-flex sm6 md4 xs12 :key="i">
            <contact-info :contact="contact" />
          </v-flex>
        </template>
      </v-layout>
      
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import PortfolioApp from "../components/PortfolioApp.vue";
import ContactInfo from "../components/ContactInfo.vue";

export default {
  name: "home",
  components: {
    // HelloWorld,
    PortfolioApp,
    ContactInfo
  },
  data() {
    return {
      aboutText:
        "I love the process of conceptualizing new web applications that make life easier for people. My biggest strengths lie in project management, building positive client relationships, and the ability to instill positivity with any team I am placed into.",
      apps: [
        {
         
          name: "Eazy-Meals",
          price: "FREE",
          logo: "eazymeals.gif",
         
          description:
            "",
          
          code: {
            name: "github",
            icon: "mdi-github",
            link: "https://github.com/TeamEazyMeals"
          }
        }
          ],
            contactLinks: [
        {
          name: "Email",
          value: "yoza.futho@gmail.com",
          link: "mailto:yoza.futho@gmail.com",
          icon: "mdi-email"
        },
        {
          name: "LinkedIn",
          value: "Yonela Futho",
          link: "https://www.linkedin.com/in/yonela-futho-60072240/",
          icon: "mdi-linkedin"
        },
        
        {
          name: "Github",
          value: "yonela986",
          link: "https://github.com/Yonela986",
          icon: "mdi-github"
        },
        {
          name: "Facebook",
          value: "Yonela Futho",
          link: "https://www.facebook.com/yoza.futho/",
          icon: "mdi-facebook"
        },
        {
          name: "Instagram",
          value: "@nela_futho",
          link: "https://www.instagram.com/nela_futho/",
          icon: "mdi-instagram"
        }
      ],
        }
    
    
    

    
  }

  

}

</script>

<template>
  <v-app>
    <!-- <v-navigation-drawer app>
      <v-row
     
      >
        <v-col
        class="profile-image"
 
        >
          <v-avatar
            class="profile"
            color="grey"
            size="164"
            tile
          >
            <v-img src="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"></v-img>
          </v-avatar>
        </v-col>
      </v-row>
 
  
    
  </v-navigation-drawer> -->

    <v-main class="aside">
      <v-row class="float-right-social">
        <v-btn icon class="icon-spacing">
          <v-icon large>mdi-linkedin</v-icon>
        </v-btn>

        <v-btn icon class="icon-spacing">
          <v-icon large>mdi-facebook</v-icon>
        </v-btn>

        <v-btn icon class="icon-spacing">
          <v-icon large>mdi-github</v-icon>
        </v-btn>

        <v-btn icon class="icon-spacing">
          <v-icon large>mdi-email-send</v-icon>
        </v-btn>
      </v-row>

      <v-row>
        <v-col md="3" sm="4" xm="12">
          <v-row class="profile-image">
            <v-avatar class="profile-image" color="grey" size="164" tile>
              <v-img
                src="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"
              ></v-img>
            </v-avatar>
          </v-row>
          <v-container fluid class="padding-filtre">
            <!-- Languages -->
            <v-row class="display-list">
              <h4 class="filtre-subtitle">Languagues</h4>
              <v-checkbox
                class="checkbox-spacing"
                v-model="checkbox1"
                :label="`Checkbox 1: ${checkbox1.toString()}`"
              ></v-checkbox>
              <v-checkbox
                class="checkbox-spacing"
                v-model="checkbox2"
                :label="`Checkbox 2: ${checkbox2.toString()}`"
              ></v-checkbox>
              <v-checkbox
                class="checkbox-spacing"
                v-model="checkbox2"
                :label="`Checkbox 2: ${checkbox2.toString()}`"
              ></v-checkbox>
            </v-row>
            <!-- Frameworks -->
            <v-row class="display-list">
              <h4 class="filtre-subtitle">Frameworks</h4>
              <v-checkbox
                class="checkbox-spacing"
                v-model="checkbox1"
                :label="`Checkbox 1: ${checkbox1.toString()}`"
              ></v-checkbox>
              <v-checkbox
                class="checkbox-spacing"
                v-model="checkbox2"
                :label="`Checkbox 2: ${checkbox2.toString()}`"
              ></v-checkbox>
              <v-checkbox
                class="checkbox-spacing"
                v-model="checkbox2"
                :label="`Checkbox 2: ${checkbox2.toString()}`"
              ></v-checkbox>
            </v-row>
            <!-- Frameworks -->
            <v-row class="display-list">
              <h4 class="filtre-subtitle">Databases</h4>
              <v-checkbox
                class="checkbox-spacing"
                v-model="checkbox1"
                :label="`Checkbox 1: ${checkbox1.toString()}`"
              ></v-checkbox>
              <v-checkbox
                class="checkbox-spacing"
                v-model="checkbox2"
                :label="`Checkbox 2: ${checkbox2.toString()}`"
              ></v-checkbox>
              <v-checkbox
                class="checkbox-spacing"
                v-model="checkbox2"
                :label="`Checkbox 2: ${checkbox2.toString()}`"
              ></v-checkbox>
            </v-row>
          </v-container>
        </v-col>
        <v-col md="9" sm="8" xs="12">
          <HelloWorld />

          <TabsList />
        </v-col>
      </v-row>
    </v-main>
    <v-footer app>
      <!-- -->
      FOOTER
    </v-footer>
  </v-app>
</template>

<script>
import TabsList from "./components/TabsList.vue";
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    TabsList,
    HelloWorld,
  },

  data() {
    return {
      checkbox1: true,
      checkbox2: false,
    };
  },
};
</script>
<style scoped>
.profile-image {
  justify-content: start;
  display: flex;

  margin-bottom: 10%;
}
.padding-filtre {
  padding: 0 0 0 0;
}
@media only screen and (max-device-width: 480px) {
  .profile-image {
    justify-content: center;
    display: flex;
    margin: 5% 0;
  }
  .padding-filtre {
    margin: 0 5%;
  }
}
.checkbox-spacing {
  margin-top: 0px;
  padding-top: 0px;
}
.filtre-subtitle {
  margin-bottom: 1rem;
}
.display-list {
  display: block;
}
.float-right-social {
  display: flex;
  justify-content: end;
  align-content: flex-end;
  width: 100%;
  height: 3.5rem;
  align-items: center;
}
.icon-spacing {
  margin-right: 5px;
}
.aside {
  margin: 0 5% 0 5%;
}
</style>

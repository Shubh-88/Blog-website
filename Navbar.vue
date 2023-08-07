<!-- eslint-disable vue/multi-word-component-names -->
<template>
 
    <v-layout>
      <v-app-bar
        color="teal-darken-4"
        image="https://picsum.photos/1920/1080?random"
      >
        <template v-slot:image>
          <v-img
            gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"
          ></v-img>
        </template>
        <v-app-bar-title >
            DEVELOPMENT BLOGS
        </v-app-bar-title>

        <v-spacer>

        </v-spacer>
 
 
 <v-toolbar-items>
        <v-btn >
          <router-link to="/">Home</router-link>
        </v-btn>

        <v-btn >
          <router-link to="/About">About</router-link>
        </v-btn>

        <v-btn >

        </v-btn>
      </v-toolbar-items>
      </v-app-bar>

      
    </v-layout>

</template>

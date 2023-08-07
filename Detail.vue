
<template>
    <h1 style="text-align: center;">Blog Details</h1>
  
    <v-container class="det">
      <v-row>
        <v-col cols="12">
          <v-card>
            <v-card-title>
                {{blog.title}}
            </v-card-title>
            <v-card-item>
              <div class="text-caption">
                {{blog.body}}
               </div>
               
              <!-- React can be used to develop single-page, mobile, or server-rendered applications with frameworks like Next.js. Because React is only concerned with the user interface and rendering components to the DOM, React applications often rely on libraries for routing and other client-side functionality.   -->
            </v-card-item>
             
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  
  </template>
  
  
  
  <script>
  import axios from 'axios'
   export default {
    data() {
      return {
        blog : "",
      }
    },
    methods:{
      readData(){
        axios.get('https://jsonplaceholder.typicode.com/posts/'+this.$route.params.id)
        .then(response => {
          this.blog = response.data;
         
        })
        .catch(error => {
          console.log(error);
        })
      }
    },
     created(){
      this.readData();
    } 
    }
   
  </script>
  <style>
.det{
    background-color: aquamarine;
}
</style>
  
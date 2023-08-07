
<template>
  <h1 style="text-align: center;">BLOGS</h1>

  <v-container class="cont">
    <v-row>
      <v-col cols="12" md="3" v-for="(item, i) in blog" :key="i">
        <v-card>
          <v-card-title>{{item.title}}</v-card-title>
          <v-card-item>
            <div class="text-caption">
              {{ item.body }}
             </div>
            <!-- React can be used to develop single-page, mobile, or server-rendered applications with frameworks like Next.js. Because React is only concerned with the user interface and rendering components to the DOM, React applications often rely on libraries for routing and other client-side functionality.   -->
          </v-card-item>
          <v-card-actions>
            <v-btn @click="BlogDetails(item.id)">
              View Blog
            </v-btn>
            <v-btn @click="BlogComments(item.id)">
             Comments
            </v-btn>
          </v-card-actions>
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
      axios.get('https://jsonplaceholder.typicode.com/posts')
      .then(response => {
        this.blog = response.data;
      })
      .catch(error => {
        console.log(error);
      })
    },
    BlogDetails(id){
      this.$router.push({name:'Detail',params:{id}});
      // alert(id);
    },
    BlogComments(id){
      this.$router.push({name:'comment',params:{id}});
 }
  },
  created(){
    this.readData();

  }
 }

</script>
<style scoped>.cont{
  background-color: rgba(9, 132, 104, 0.856);
}
</style>

<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <h1 class="text-center mt-3 mb-3">THIS IS ABOUT PAGE</h1>
  <hr style="height: 2px; opacity: 0.5;">
  <v-card   variant="tonal" class="round ml-4 mr-4 mt-4" :elevation="2">
  <v-card-title> <strong><h3 class="text-center mt-3">Blog Website </h3></strong></v-card-title>
  <v-card-text>
   <p class="text-h6 font-italic" > Welcome to our blog website, where insightful articles and engaging discussions come together to create a vibrant community. Powered by Vue.js and Bootstrap, we've crafted a user-friendly platform that seamlessly blends functionality and aesthetics.
    At Blog-in, we are passionate about creating a space for knowledge-sharing and meaningful conversations. Our team of dedicated writers and developers work tirelessly to curate compelling content that covers a wide array of topics, ensuring there's something for everyone.</p> 
   <br>
   <br>
    <p class="text-h6 font-italic">
    Our website's dynamic interface is made possible by the integration of Vue.js and Bootstrap. With Vue.js, we can deliver a seamless browsing experience, allowing you to navigate through our content effortlessly. Meanwhile, Bootstrap ensures that the site is fully responsive, adapting perfectly to different devices and screen sizes.
    Thank you for being a part of Blog-in. We look forward to embarking on this enriching journey of knowledge and camaraderie with you!
   </p>
   <br>
   <br>
   <h2> ** In this site we can only see the fake api data of the blogs! **</h2>
  </v-card-text>

  </v-card>
  <br>

  <div class="flip-card ml-5">
  <div class="flip-card-inner">
    <div class="flip-card-front">
      <img src="https://imgs.search.brave.com/rI_hwDDrgC__RJOo4pM0UWRMwkfKyRXsaFlDAr14PSU/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9sb2dv/dHlwLnVzL2ZpbGUv/dnVlLWpzLnN2Zw.svg">
    </div>
    <div class="flip-card-back ">
      <h1 class="mt-4">Vue.js</h1>
      <p>Vue.js is a popular open-source JavaScript framework used for building user interfaces and single-page applications (SPAs). </p>
      
    </div>
 
  </div>
</div>

<div class="flip-card ml-5">
  <div class="flip-card-inner">
    <div class="flip-card-front ">
      <img src="https://cdn.iconscout.com/icon/free/png-256/free-bootstrap-1-226079.png?f=webp&w=128">
    </div>
    <div class="flip-card-back ">
      <h1 class="mt-4">Bootstrap</h1>
      <p>Vue.js is a popular open-source JavaScript framework used for building user interfaces and single-page applications (SPAs). </p>
    
    </div>
  </div>
</div>

</template>

<!--Styling-->
<style>

.flip-card {
  background-color: transparent;
  width: 300px;
  height: 200px;
  border: 1px solid #f1f1f1;
  display: inline-block;
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

/* Position the front and back side */
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
}

/* Style the front side (fallback if image is missing) */
.flip-card-front {
  background-color: #bbb;
  color: black;
}

/* Style the back side */
.flip-card-back {
  background-color: dodgerblue;
  color: white;
  transform: rotateY(180deg);
}

</style>

   
  
   
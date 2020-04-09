<template>
  <div class="home">
    <h1> Future Memories </h1>
    <!-- <section class="image-gallery">
      <div class="image" v-for="item in items" :key="item.id">
        <h2>{{item.title}}</h2>
        <img :src="item.path" >
        <p> {{item.description}} </p>
      </div>
    </section> -->
<ol>
        <li>OOXXOOXOXXX</li>
        <li>Get Married </li>
        <li>WATCH STARGATE!!!</li>
        <li>Watch all the Star Wars movies</li>
        <li>Beat Ben's parents at ping pong</li>
        <li>Hot springs</li>
        <li>Hammocking</li>
        <li>Road trips </li>
        <li>Watch Sasquatch Gang...again</li>
        <li>All nighter</li>
        <li>Bridge jump into the Payette River</li>
        <li>Watch the sunrise</li>
        <li>Effectively get Kaitlyn to wake up early enough to watch the sunrise</li>
        <li>Shoot stuff</li>
        <li>Zion's</li>
        <li>Take Ben jet skiing</li>
</ol>
  </div>
</template>

// <script>
// // @ is an alias to /src
// import axios from 'axios';
// export default {
//   name: 'Future',
//   data() {
//   return {
//    items: [],
//   }
// },
// created() {
//     this.getItems();
//   },
//   methods: {
//     async getItems() {
//       try {
//         let response = await axios.get("/api/items");
//         this.items = response.data;
//         return true;
//       } catch (error) {
//         console.log(error);
//       }
//     },
//   }
// }
// </script>
<style scoped>

.home li {
  text-align: left;
}

/* Masonry on large screens */
@media only screen and (min-width: 1024px) {
  .image-gallery {
    column-count: 4;
  }
}

/* Masonry on medium-sized screens */
@media only screen and (max-width: 1023px) and (min-width: 768px) {
  .image-gallery {
    column-count: 3;
  }
}

/* Masonry on small screens */
@media only screen and (max-width: 767px) and (min-width: 540px) {
  .image-gallery {
    column-count: 2;
  }
}
</style>

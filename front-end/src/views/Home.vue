<template>
  <div class="home">
    <h1> Favorite Memories </h1>
    <section class="image-gallery">
      <div class="image" v-for="item in items" :key="item.id">
        <h2>{{item.title}}</h2>
        <img :src="item.path" >
        <p> {{item.description}} </p>
      </div>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import axios from 'axios';
export default {
  name: 'Home',
  data() {
  return {
   items: [],
  }
},
created() {
    this.getItems();
  },
  methods: {
    async getItems() {
      try {
        let response = await axios.get("/api/items");
        this.items = response.data;
        return true;
      } catch (error) {
        console.log(error);
      }
    },
  }
}
</script>
<style scoped>
.image h2 {
  font-style: italic;
}

/* Masonry */
*,
*:before,
*:after {
  box-sizing: inherit;
}

.image-gallery {
  column-gap: 1.5em;
  padding-top:20px;
}

.image {
  margin: 1em 0 1.5em;
  display: inline-block;
  width: 100%;
  color: #FFFF66;
  outline-width: 10px;
  outline:solid;
}
.image p {
  color:black;
}
.image h2 {
  color:black;
}

.image img {
  max-width: 100%;
  transform:rotate(90deg);
  padding-top: 60px;
  padding-bottom: 60px;

  text-align: center;

}
.image {
text-align: center;
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

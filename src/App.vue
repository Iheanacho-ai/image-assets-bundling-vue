<template>
  <div>
    <h2>My Gallery</h2>
    <div class="image-container">
      <div class="image" v-for = "image in images" :key="image">
        <img :src="image">
      </div>
    </div>
  </div>
</template>

<script>
  import Img1 from './assets/photo-1.jpg'
  import Img2 from './assets/photo-2.jpg'
  import Img3 from './assets/photo-3.jpg'
  import Img4 from './assets/photo-4.jpg'
  import Img5 from './assets/photo-5.jpg'
  import Img6 from './assets/photo-6.jpg'
  import Img7 from './assets/photo-7.jpg'
  import Img8 from './assets/photo-8.jpg'
  import Img9 from './assets/photo-9.jpg'

  export default {
    data(){
      return{
        images: [Img1, Img2, Img3, Img4, Img5, Img6, Img7, Img8, Img9]
      }
    },
  }
</script>

<style>

#app {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
h2{
  text-align: center;
}
.image-container{
  width: 80%;
  margin-left: 10%;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 5px;

}
.image-container div:first-child {
  grid-column-start: 1;
  grid-column-end: 3;
}
.image-container div:last-child {
  grid-row-start: 2;
  grid-row-end: 5;
}
.image{
  width: 100%;
  height: 300px;
}
.image img {
  width: 100%;
  height: 100%;
}


</style>

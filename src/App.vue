<template>
  <div id="app">
      <Vuelightbox id="mylightbox"
        :images="images"
        :image_class=" 'img-responsive img-rounded' "
        :album_class=" 'my-album-class' "
        :options="options">
      </Vuelightbox>
      <button @click="push">Add an Image</button<
  </div>
</template>

<script>
  import Vuelightbox from '../src/index'
  export default {
    name: 'MainApp',
    components: {
      Vuelightbox
    },
    data(){
      return{
        images : [
          {
              src : 'https://cdn.rawgit.com/vrajroham/vrajroham.github.io/85d64ac5/imgs/img1.jpg',
              title : 'Image 2'
          },
          {
              src : 'https://cdn.rawgit.com/vrajroham/vrajroham.github.io/85d64ac5/imgs/img2.jpg',
              title : 'Image 3'
          },
          {
              src : 'https://cdn.rawgit.com/vrajroham/vrajroham.github.io/85d64ac5/imgs/img3.jpg',
              title : ''
          },
        ],
        options : {
            closeText : 'X'
            }
      }
    },
    methods: {
      push: function() {
        this.images.push({
              src : 'https://cdn.rawgit.com/vrajroham/vrajroham.github.io/85d64ac5/imgs/img4.jpg',
              title : ''
          });
      }
    },
    mounted() {

    }
  }
</script>

<style>

</style>

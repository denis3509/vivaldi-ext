<template>
  <div
          class="launcher"
          :style="styleObj"
  >


  </div>
</template>

<script>
import config from '../../config'

  export default {
    name: 'index',
    data : function () {
      return {
        styleObj : {
          backgroundImage : 'url(./background2.jpg)',
          backgroundPosition : '80%',
          height : window.innerHeight + 'px',
          backgroundAttachment : 'fixed',
          backgroundSize : 'cover',
        }
      }
    },
    mounted() {
      this.$nextTick(() => {
        window.addEventListener('resize', this.onResize);
      })
    },

    beforeDestroy() {
      window.removeEventListener('resize', this.onResize);
    },

    methods: {
      onResize() {
        this.styleObj.windowHeight = window.innerHeight
      }
    }
  }
</script>

<style scoped>
 .launcher {
   width : 100%;

 }
</style>
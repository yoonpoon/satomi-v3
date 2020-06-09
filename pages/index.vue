<template>
  <div class="mx-auto">
    <Info/>
    <Footer/>
  </div>
</template>

<script>
import Info from '~/components/Info.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Info,
    Footer
  }
};
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>

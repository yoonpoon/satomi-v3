<template>
  <section :style="{ backgroundColor: this.selectRandomBgColor }">
    <div class="mx-auto p-5">
      <Nav />
      <nuxt />
    </div>
  </section>
</template>

<script>
import Nav from "~/components/Nav.vue";

export default {
  data() {
    return {
      bgColors: ["#E5DCE3", "#FFF", "#EED2BD"],
      selectBgColor: {
        color: null
      }
    };
  },
  mounted() {
    this.getRandomBgColor()
  },
  computed: {
    selectRandomBgColor() {
      return (this.selectBgColor.color =
        this.bgColors[this.selectBgColor.color] || null);
    }
  },
  methods: {
    getRandomBgColor() {
      return (this.selectBgColor.color = Math.floor(
        Math.random() * this.bgColors.length
      ));
    }
  },
  components: {
    Nav
  }
};
</script>

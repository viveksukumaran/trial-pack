<template>
  <div class="trial-pack">
    <div>Choose size</div>
    <div>
    <label v-for="detail in images" v-bind:key="detail.size">
      <input
        type="radio"
        name="size"
        v-model="selectedSize"
        v-bind:value="detail.size"
        v-on:click="changeImg(detail)"
      />
      {{detail.size}}
    </label></div>
    <img :src="selectedImage" />
  </div>
</template>

<script>
export default {
  name: "TrialPack",
  data() {
    return {
      images: [
        { size: "1(2-5 KG)", image: "/assets/lillydoo-testpaket-10.jpg" },
        { size: "2(4-8 KG)", image: "/assets/lillydoo-testpaket-20.jpg" },
        { size: "3(6-10 KG)", image: "/assets/lillydoo-testpaket-30.jpg" },
        { size: "4(9-14 KG)", image: "/assets/lillydoo-testpaket-40.jpg" },
        { size: "5(11-16 KG)", image: "/assets/lillydoo-testpaket-50.jpg" }
      ],
      selectedImage: "/assets/lillydoo-testpaket-10.jpg",
      selectedSize: "1(2-5 KG)"      
    };
  },
  methods: {
    changeImg(source) {
      this.selectedImage = source.image;
      this.selectedSize = source.size;
    }
  }
};
// this.selected = this.images[0];
</script>
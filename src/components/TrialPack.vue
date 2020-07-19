<template>
  <b-container>
    <b-row align-v="start">
      <b-col>        
        <b-img :src="selectedImage" fluid alt="Responsive image"></b-img>        
      </b-col>
      <b-col>
        <b-row class="mt-2">
          <h3>Discover our skin friendliness</h3>
        </b-row>
        <b-row class="mt-2">  
          CHOOSE YOUR SIZE
        </b-row>
        <b-row class="mt-2">
        <b-form-group>
        <b-form-radio-group
        class="d-flex"
          id="btn-radios-2"
          v-model="selected"
          :options="options"
          buttons
          button-variant="outline-secondary"
          name="radio-btn-outline"
          v-on:change="changeSize">
        </b-form-radio-group>
        </b-form-group>
        </b-row>
      <b-row class="text-justify mb-2">
        Now test our skin-friendly nappies and get our wet wipes with 99% water to size 1 - 3 or the sensitive wet wipes to size 4 - 5.
      </b-row>
      <b-row class="text-justify mt-2">
        <ul>
          <li>We pay the products, you only ship.</li>
          <li class="text-muted">Automatic transition to the cancellable diaper subscription for &euro;49.50 per delivery.</li>
          <li>Prices incl. VAT, if applicable plus <a class="text-muted" href="https://www.lillydoo.com/de/zahlung-und-versand">shipping costs</a></li>
        </ul>
      </b-row>
      <b-row>
        <b-button block variant="secondary">PUT IN THE SHOPPING CART</b-button>
      </b-row>      
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: "TrialPack",
  data() {
    return {
      selectedImage: "/assets/lillydoo-testpaket-10.jpg",      
      selected: 'radio1',
      options: [
        { text: '1 (2-5 KG)', value: 'radio1', image: "/assets/lillydoo-testpaket-10.jpg" },
        { text: '2 (4-8 KG)', value: 'radio2', image: "/assets/lillydoo-testpaket-20.jpg" },
        { text: '3 (6-10 KG)', value: 'radio3', image: "/assets/lillydoo-testpaket-30.jpg" },
        { text: '4 (9-14 KG)', value: 'radio4', image: "/assets/lillydoo-testpaket-40.jpg" },
        { text: '5 (11-16 KG)', value: 'radio5', image: "/assets/lillydoo-testpaket-50.jpg" },
      ]
    };
  },
  methods: {
    changeSize(checked) {
      this.selectedImage = this.options.find(option => option.value===checked).image;    
    }
  }
};
</script>
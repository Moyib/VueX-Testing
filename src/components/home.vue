<template>
  <div class="home">
    <h4>Coffee first. Schemes later.</h4>
    <div class="row">
      <div class="col-md-4 col-lg4" v-for="(data, index) in products" :key="index">
        <img :src="data.image" class="img-fluid">
        <h5>{{ data.productName }}</h5>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
  data() {
    return { 
      title: 'home',
      products: [
        {
          productName: "Latte",
          image: require('../assets/latte-coffee.jpg')
        },
        {
          productName: "Capuccino",
          image: require('../assets/capuccino.jpg')
        },
        {
          productName: "Espresso",
          image: require('../assets/espresso.jpg')
        },
        {
          productName: "Coffee Crust",
          image: require('../assets/burnt-coffee.jpg')
        },
        {
          productName: "Machiato",
          image: require('../assets/machiato.jpg')
        },
        {
          productName: "Mochiato",
          image: require('../assets/mochiato.jpg')
        }
    
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.home {
  color: white;
  margin: 3rem;
}

h4 {
  margin-top: 8.4rem;
  margin-bottom: 1.7rem;
}

h5 {
  margin: 2rem;
}
img {
  margin: 1rem;
  border-radius: 1rem;
  cursor: pointer;
}
</style>

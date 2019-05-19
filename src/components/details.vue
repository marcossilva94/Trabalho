<template>
  <div id="details" class="details">
    <div class="cart col-md-3 offset-md-10">
      <i class="fas fa-shopping-cart">({{cart}})</i>
    </div>
    <div class="container">
      <div class="row" v-for="(product,index) in products" :key="index">
        <div class="col-md-6" v-if="proId == product.productId">
          <h1>{{product.productTitle}}</h1>
          <img :src="product.image" class="img-fluid">
        </div>
        <div class="col-md-6" v-if="proId == product.productId">
          <h3>{{product.detalhes}}</h3>
          <div class="center">
            <button v-on:click="addToCart" class="btn btn-warning fas fa-shopping-cart">Comprar</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "details",
  data() {
    return {
      proId: this.$route.params.Pid,
      title: "details",
      cart: 0,

      products: [
        {
          productTitle: "moto g7",
          image: require("../assets/images/motog7.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 1
        },
        {
          productTitle: "a50",
          image: require("../assets/images/a50.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 2
        },
        {
          productTitle: "s8",
          image: require("../assets/images/s8.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 3
        },
        {
          productTitle: "EFG",
          image: require("../assets/images/lgk12.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 4
        },
        {
          productTitle: "MLI",
          image: require("../assets/images/acessorios.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 5
        },
        {
          productTitle: "Banans",
          image: require("../assets/images/s8.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 6
        },
        {
          productTitle: "ABCN",
          image: require("../assets/images/motog7.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 7
        },
        {
          productTitle: "KARMA",
          image: require("../assets/images/a50.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 8
        },
        {
          productTitle: "Tino",
          image: require("../assets/images/s8.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 9
        },
        {
          productTitle: "EFG",
          image: require("../assets/images/s8.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 10
        },
        {
          productTitle: "MLI",
          image: require("../assets/images/s8.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 11
        },
        {
          productTitle: "Banans",
          image: require("../assets/images/s8.jpg"),
          detalhes:
            "Smartphone Motorola Moto G7 Play 32GB Dual Chip Android Pie" +
            "- 9.0 Tela 5.7' 1.8 GHz Octa-Core 4G Câmera 13MP - Indigo",
          productId: 12
        }
      ]
    };
  },
  methods: {
    addToCart() {
      this.cart += 1;
    }
  }
};
</script>
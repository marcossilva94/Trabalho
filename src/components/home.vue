<template>
  <div class="home">
      <div class="row">
			<div class="col-md-3 col-lg3">
           <div class="carousel-item active">						
            <img class="d-block w-100" src="../assets/images/s10.jpg" alt="First slide">
           </div>
           <div class="carousel-item active">						
            <img class="d-block w-100" src="../assets/images/s10.jpg" alt="Second slide">
           </div>
    </div>
			<div class="col-md-6 carousel slide">
          <h2>Smartphones</h2>
					<div class="card-body">
            Conheça os celulares com alta tecnologia e design sofisticado para satisfazer
            suas necessidades e possibilitar uma melhor comodidade ao seu dia-a-dia
					</div>
			</div>
		</div>
    <hr>
    <h1>{{title}}</h1>
    <div class="row">
      <div class="col-md-2 col-lg2 border border-warning" v-for="(data,index) in products" :key="index">
        <img :src="data.image" class="img-fluid">
         <h3 @click="goTodetail(data.productId)" >{{data.productTitle}}</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      title: 'Destaques',
      products:[
      {
        productTitle:"moto g7",
        image       : require('../assets/images/motog7.jpg'),
        productId:1
      },
      {
        productTitle:"a50",
        image       : require('../assets/images/a50.jpg'),
        productId:2
      },
      {
        productTitle:"s8",
        image       : require('../assets/images/s8.jpg'),
        productId:3
      },
      {
        productTitle:"EFG",
        image       : require('../assets/images/lgk12.jpg'),
        productId:4
      },
      {
        productTitle:"MLI",
        image       : require('../assets/images/acessorios.jpg'),
        productId:5
      },
      {
        productTitle:"Banans",
        image       : require('../assets/images/s8.jpg'),
        productId:6
      },
      {
        productTitle:"ABCN",
        image       : require('../assets/images/motog7.jpg'),
        productId:7
      },
      {
        productTitle:"KARMA",
        image       : require('../assets/images/a50.jpg'),
        productId:8
      },
      {
        productTitle:"Tino",
        image       : require('../assets/images/s8.jpg'),
        productId:9
      },
      {
        productTitle:"EFG",
        image       : require('../assets/images/s8.jpg'),
        productId:10
      },
      {
        productTitle:"MLI",
        image       : require('../assets/images/s8.jpg'),
        productId:11
      },
      {
        productTitle:"Banans",
        image       : require('../assets/images/s8.jpg'),
        productId:12
      }]
    }
  },
  methods:{
  goTodetail(prodId) {
    let proId=prodId
    this.$router.push({name:'details',params:{Pid:proId}})
  }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.row img{
  max-height: 15em;
  width: 100%;

}
.row h3{
  cursor:pointer;
}
</style>

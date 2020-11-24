<template>
<div>
    <h2>{{gabungKata}}</h2>
    <!-- v-text -->
    <h1 v-text="lastName"></h1>
    <!-- v-html -->
    <div v-html="lastName"></div>
    <!-- v-bind -->
    <h1 class="count">{{count}}</h1>
    <p>ini nilai saya</p>
    <button v-on:click="addCount">tambah</button>
    <!-- <img v-bind:src="img" alt="" srcset=""> -->
    <br>
    <input type="text" name="name" v-bind:value="title" id="">
    <ul>
      <li v-for="(data, index) in filterFood" v-bind:key="index">
        <h4 v-if="data.price >= 22000">{{data.name.toUpperCase()}} <span>|| {{data.price + 5000}}</span></h4>
        </li>
    </ul>
    <h1 v-if="count === 1">ini nilinya 1</h1>
    <h2 v-else-if="count === 2"> ini nilai 2</h2>
    <h1 v-else>ini nilainya terlalu besar</h1>
    <hr>
    <h6>email : {{email}}</h6>
    <h6>password : {{password}}</h6>
    <h6>kelas : {{kelas}}</h6>
     <input type="text" name="email" v-model="email">
      <input type="password" v-model="password" placeholder="password">
      <select v-model="kelas">
        <option value="web1">web1</option>
        <option value="web2">web2</option>
        <option value="web3">web3</option>
        <option value="web4">web4</option>
        <option value="web5">web5</option>
      </select>
</div>
</template>

<script>
export default {
  name: 'Home',
  data: function () {
    return {
      email: '',
      kelas: '',
      password: '',
      count: 1,
      fistName: 'bla bla',
      lastName: 'akbar',
      img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png',
      title: 'belajar vue js',
      foods: [
        { id: 1, name: 'nasi goreng', price: 30000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' },
        { id: 2, name: 'nasi uduk', price: 20000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' },
        { id: 3, name: 'nasi padng', price: 10000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' },
        { id: 4, name: 'jus goreng', price: 25000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' },
        { id: 4, name: 'jus jeruk', price: 50000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' }
      ]
    }
  },
  methods: {
    sayHello: function () {
      alert('hello world')
    },
    addCount () {
      this.count = this.count + 1
    },
    handleChange (e) {
      this.email = e.target.value
    }
  },
  computed: {
    gabungKata () {
      return this.fistName + ' ' + this.lastName
    },
    filterFood () {
      const dataFilter = this.foods.filter((item) => item.price > 22000)
      return dataFilter
    }
  }
}
</script>

<style scoped>
  .count{
    color: red;
  }
</style>

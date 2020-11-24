<template>
  <div>
    <Button name="simpan" type="warning"/>
    <Navbar />
    <div class="row mt-5">
      <div class="col-md-3 mt-2" v-for="food in foods" :key=food.id>
      <Card :data=food  />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from '../components/module/Navbar'
import Footer from '../components/module/Footer'
import Card from '../components/module/Card'
import Button from '../components/base/Button'
// import Footer from '../components/module/Navbar'

export default {
  name: 'Coba',
  components: {
    Navbar,
    Footer,
    Card,
    Button
  },
  data: function () {
    return {
      judulFooter: 'helo ini web saya 1111',
      foods: [
        { id: 1, name: 'nasi goreng', price: 30000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' },
        { id: 2, name: 'nasi uduk', price: 20000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' },
        { id: 3, name: 'nasi padng', price: 10000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' },
        { id: 4, name: 'jus goreng', price: 25000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' },
        { id: 5, name: 'jus jeruk', price: 50000, img: 'https://photo.jpnn.com/arsip/watermark/2019/12/15/lomba-menggambar-ilustrasi-foto-pixabaycom-54.png' }
      ]
    }
  }
}
</script>
<style scoped>

</style>

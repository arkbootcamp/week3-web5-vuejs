<template>
  <div class="wrapper-footer">
    <h5>{{judul}}</h5>
  </div>
</template>

<script>
export default {
  props: {
    judul: {
      type: String,
      default: 'ini footer'
    }
  }
}
</script>

<style scoped>
.wrapper-footer{
  display: flex;
  height: 120px;
  width: 100%;
  background-color: salmon;
  align-items: center;
  justify-content: center;
}
.wrapper-footer h5{
  color: red;
  font-size: 16px;
  text-align: center;
}
</style>

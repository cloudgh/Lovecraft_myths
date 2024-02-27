<template>
  <div class="header">
    <button  @click="goTo('/')">Главная</button>
    <button  @click="goTo('/page2')">Отец чудовищ</button>
    <button  @click="goTo('/page3')">Cyщества</button>
  </div>
</template>
<script>
export default {
    methods: {
      goTo(route) {
        this.$router.push(route);
      }
    }
  }
</script>

<style lang="scss" scoped>
.header {
  color: #fff;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  button {
    width: 200px;
    background-color: #233C80bf;
    border-radius: 30px;
    border-left: 2px solid  #7FD6FC;
    border-top: 4px solid  #7FD6FC;
    border-right: 2px solid #1D3356;
    border-bottom: 4px solid #1D3356;
    color: #fff;
    padding: 10px 20px;
    font-size: 12pt;
    cursor: pointer;
    text-decoration: none;
    margin: 10px;
  }
}
</style>
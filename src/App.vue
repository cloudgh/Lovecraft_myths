<template>
    <nav>
      <ul class="nav">
        <li><router-link to="/">Главная</router-link></li>
        <li><router-link to="/page2">Отец чудовищ</router-link></li>
        <li><router-link to="/page3">Существа</router-link></li>
      </ul>
    </nav>
    <router-view/>
  </template>

<script>
</script>
<style lang ="scss">
*{
    margin-top: 0px;
    padding: 0;
    box-sizing: border-box;
    margin-bottom: 0px;
    margin-left: 0px;
    margin-right: 0px;
}
nav {
  display: flex;
  align-items: center;
  justify-content: center;
 
}
.nav{
  display: flex;
  flex-direction: row;
  list-style-type:none;
}
.nav li a{
  background-color: #233C80bf;
  border-radius: 30px;
  border-left: 2px solid  #166b90;
  border-top: 4px solid  #166b90;
  border-right: 2px solid #1D3356;
  border-bottom: 4px solid #1D3356;
  display: block;
  position: relative;
  text-decoration: none;
  text-align: center;
  padding: 2px 5px;
  font-size: 20px;
  margin:  20px 5px 0 5px;
  color: #fff;
  
  transition: 0.5s;
  @media (max-width: 480px) {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 60px;
    margin:  10px 5px 0 5px;
  }
}

@media (hover: hover) {
  .nav:hover li a {
    transform: scale(1.5);
    opacity: 0.2;
    filter: blur(5px);
  }

  .nav li a:hover {
    transform: scale(2);
    opacity: 1;
    filter: blur(0);
    text-decoration: none;
    color: aquamarine;
  }
}

</style>
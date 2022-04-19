<template>
  <div class="consoleComponent">
    <div class="contentBox">
      <img class="poster" :src="poster" alt="poster">
    </div>
      <a class="button" :href="`${publicPath}LUNAZUL.pdf`" download>DESCARGAR</a>
  </div>
</template>

<script>
import poster from '../assets/lunazul.jpg';

export default {
  name: 'HelloWorld',
  data() {
    return {
      poster,
      publicPath: process.env.BASE_URL,
    }
  },
  methods: {
  }
}
</script>

<style scoped>
.consoleComponent {
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background: #00A8FF;
}

.contentBox {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 70%;
  height: 80%;
  border: 1px solid black;
}

.poster {
  width: 30%;
  height: 80%;
  position: absolute;
}

.title {
  position: absolute;
  top: 5%;
  font-size: 50px;
  color: #fff;
}

.consoleBox {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  flex-wrap: wrap;
  width: 60%;
  height: 40%;
  border: 4px solid #fff;
  border-radius: 10px;
}

.consoleButtons {
  width: 6%;
  height: 20%;
  border: 4px solid #fff;
  border-radius: 10px;
  background: transparent;
  cursor: pointer;
  outline: none;
  color: #fff;
}

.pressed:active {
  background: #fff;
}

@media (max-width: 768px) {
  .title {
    position: absolute;
    top: 8%;
    font-size: 40px;
    color: #fff;
}

  .consoleBox {
    position: absolute;
    top: 25%;
    left: 20%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    flex-wrap: wrap;
    width: 60%;
    height: 60%;
    border: 4px solid #fff;
    border-radius: 10px;
}

  .consoleButtons {
    width: 40%;
    height: 20%;
    border: 4px solid #fff;
    border-radius: 10px;
    background: transparent;
    cursor: pointer;
    outline: none;
    color: #fff;
}
}
</style>

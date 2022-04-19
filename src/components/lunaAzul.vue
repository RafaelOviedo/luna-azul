<template>
  <div class="consoleComponent">
    <h1 class="title">Luna Azul</h1>
    <div class="contentBox">
      <img class="poster" :src="poster" alt="poster">
      <div class="textBox">
        <p class="bookText">
          Este libro lo escribi cuando estudiaba comunicacion social, tiene casi 10 años, el estilo literario no es el mejor<br>
          pero hay una historia de ficcion interesante segun los que lo leyeron y me dieron feedback.
          <br>
          <br>
          <b><u>Sinopsis</u></b>
          <br>
          <br>
          Luego de la última guerra, sale a la luz una clandestina ciudad subterránea que le 
          cambiará la vida a dos humildes sobrevivientes, donde tras una larga dictadura de 
          más de 40 años es alterada por la avidez de escapar a la filosofía de la voluntad 
          del ser.
        </p>
      </div>
    </div>
      <a class="button" :href="`${publicPath}LUNAZUL.pdf`" download><b>DESCARGAR PDF</b></a>
  </div>
</template>

<script>
import poster from '../assets/lunazul.jpg';

export default {
  name: 'LunaAzul',
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
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background: #00A8FF;
}

.title {
  position: absolute;
  top: 5%;
  left: 46%;
  font-size: 40px;
  color: #fff;
}

.poster {
  position: absolute;
  top: 18%;
  left: 22%;
  width: 22%;
  height: 70%;
  border-radius: 15px;
}

.textBox {
  position: absolute;
  top: 15%;
  left: 58%;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 25%;
  height: 60%;
}

.bookText {
  text-align: justify;
  font-size: 20px;
  color: #fff;
}

.button {
  position: absolute;
  top: 75%;
  left: 63%;
  font-size: 19px;
  text-decoration: none;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 15%;
  height: 7%;
  color: #00A8FF;
  background: #fff;
  border-radius: 10px;
}

@media (max-width: 768px) {
  .consoleComponent {
    overflow: scroll;
  }
  .title {
    position: absolute;
    top: 2%;
    left: 31%;
    font-size: 30px;
    color: #fff;
}
  .poster {
    position: absolute;
    top: 15%;
    left: 9%;
    width: 80%;
    height: 75%;
    border-radius: 15px;
}
  .textBox {
    display: flex;
    align-items: center;
    position: absolute;
    top: 95%;
    left: 0%;
    width: 99%;
    height: 70%;
  }
  .bookText {
    position: relative;
    top: 0%;
    left: 0%;
    width: 90%;
    font-size: 20px;
  }
  .button {
    position: absolute;
    top: 167%;
    left: 16%;
    width: 65%;
    height: 7%;
  }
}
</style>

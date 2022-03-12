<template>
  <section>
    <div class="container">
    <h1 >Ask your question to magic 8 ball!!</h1>
    <div :class="{animate: animatePro}" >
    <img src="./Imges/pngfind.com-magic-8-ball-png-6164006.png">
    <the-circales :answer="answers"></the-circales>
    </div>
    <the-button class="container" @click="timeOut"></the-button>
  </div>
  </section>
</template>

<script>
import TheCircales from "./components/TheCircales.vue";
import TheButton from "./components/TheButton.vue";


export default {
  components : {
    TheCircales,
    TheButton,

    
  },
  data(){
    return{
      answers : '',
      animatePro:false
    }
  },
  provide(){
    return{
      answers:this.answers

    }
  },
  methods:{
      timeOut(){
        this.answers = '' ;
        setTimeout( this.takeRandomNumber
      ,500);
      this.animatePro = true

  },
      takeRandomNumber(){
        const randomNumber = Math.random();
        this.takeRandomString(randomNumber);
        this.animatePro = false

      },
      takeRandomString(randomNumber){
        if(randomNumber<0.05)
        {
          this.answers = 'It is certain'
        }
        else if (randomNumber<0.10) {
          this.answers = 'It is decidedly so'
        }
        else if (randomNumber<0.15) {
          this.answers = ' Without a doubt'
        }
        else if (randomNumber<0.20) {
          this.answers = 'Yes definitely'
        }
        else if (randomNumber<0.25) {
          this.answers = 'You may rely on it'
        }
        else if (randomNumber<0.30) {
          this.answers = 'As I see it, yes'
        }
        else if (randomNumber<0.35) {
          this.answers = 'Most likely'
        }
        else if (randomNumber<0.40) {
          this.answers = 'Outlook good'
        }
        else if (randomNumber<0.45) {
          this.answers = 'Yes'
        }
        else if (randomNumber<0.50) {
          this.answers = 'Signs point to yes'
        }
        else if (randomNumber<0.55) {
          this.answers = 'Reply hazy, try again'
        }
        else if (randomNumber<0.60) {
          this.answers = 'Ask again later'
        }
        else if (randomNumber<0.65) {
          this.answers = 'Better not tell you now'
        }
        else if (randomNumber<0.70) {
          this.answers = 'Cannot predict now'
        }
        else if (randomNumber<0.75) {
          this.answers = 'Concentrate and ask again'
        }
        else if (randomNumber<0.80) {
          this.answers = 'Do not count on it'
        }
        else if (randomNumber<0.85) {
          this.answers = 'My reply is no'
        }
        else if (randomNumber<0.90) {
          this.answers = 'My sources say no'
        }
        else if (randomNumber<0.95) {
          this.answers = 'Outlook not so good'
        }
        else  {
          this.answers = 'Very doubtful'
        }
      }
    }
  
}
</script>

<style>



body {
  margin: 0px;
  padding: 0px;
  font-family: Orbitron;
}

*{
  box-sizing: border-box;

}

section{
    margin: 0px auto;
    height: 100vh;
    width: 100vh;
    overflow: hidden;
}

img{
  display: flex;
  justify-content: center;
  align-items: center;
  height: 600px;
  width: 600px;
}

h1{
  margin-left: 5% ;
  font-size: 40px;
}

.container{
  transform: translate(20%);
}

.animate{
  animation: animation 0.1s ease infinite;
}

@keyframes animation {
  0% {
    transform: translate(0%);
  }
  50%{
    transform: translate(1.5%);
  }
  100%{
    transform: translate(0%);
  }
}

</style>

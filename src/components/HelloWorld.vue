<template>
  <div class="hello">

<input v-model="message" placeholder="type your name here!">

<h3>Thanks for listening to my presentation</h3>
<transition name="fade">
  <h1 class="the-message">{{ message }}</h1>
</transition>
<h3 style="margin-top: 0;">Hope you have a great rest of your friday!</h3>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    message: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
input {
  font-family: 'Fredoka One', cursive;
  height: 100px;
  font-size: 30px;
  text-align: center;
  border-radius: 4px;
  width: 50vw;
}

h1 {
  font-family: 'Fredoka One', cursive;
  font-size: 90px;
}
h3 {
  font-family: 'Fredoka One', cursive;
  font-size: 40px;
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}

.the-message {
   display: inline-block;
  animation: woah 2s linear infinite alternate;
}

@keyframes woah {
   0% { color: grey; }
  75% { color: black; }
 100% { transform: translateX(50%); color: purple; }
}
</style>

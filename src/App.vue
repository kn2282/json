<template>
  <div>
    <h1>{{ title }} {{nr*nr}} times</h1>
    <input type="text" v-model="title">
    <button @click="iAmClicked()">Click me!</button>
    <button @click="reset()">reset</button>
    <h2>{{qwerty}}</h2>
    <button @click="iAmClicked()"><input type="text" v-model="qwerty"></button>
    <br>
    <h2></h2><button @click="changeMood()">how are u?</button></div></h2>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: 'PRYMUS',
        qwerty: 'happy',
        nr: 0,
        i: false

      }
    },
    methods: {
      iAmClicked() {
        this.title = 'Clicked';
        this.nr = this.nr + 1;

      },
      reset() {
        this.nr = 0;
      },
      changeMood(){
        this.i = ! this.i;
        this.qwerty = this.i ? 'happy' : 'sad';
      }
    }
  };
</script>

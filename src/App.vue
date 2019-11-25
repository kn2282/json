<template>
  <div>
    <h1>{{ title }} {{nr}} times</h1>
    <input type="text" v-model="title">
    <h2>{{qwerty}}</h2>
    <button @click="iAmClicked()"><input type="text" v-model="qwerty"></button>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        title: 'PRYMUS',
        qwerty: 'coś tam',
        nr: 0
      }
    },
    methods: {
      iAmClicked() {
        this.title = 'Clicked';
        nr = nr+1;
      }
    }
  };
</script>

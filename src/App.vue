<template>
  <div>
    <h1 >Nasi uczestnicy:</h1>
    <div v-if="parti.lengt = 0">na razie lista pusta</div>
    <ol v-if="parti.length > 0">
      <li :key="par" v-for="par in parti">{{ par }}  <button @click="remove(par)">remove</button></li>
    </ol>
    <h3>Name:</h3>
    <input type="text" v-model="imie">
    <br>
    <h3>Surname:</h3>
    <input type="text" v-model="nazwisko">
    <button @click="addNew()">Add new participant</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        parti: [
                'Robim Hood',
                'Czak Norris',
                'Jerzy Waszyngton'
        ],
        tab: [],
        i: 0,
        imie: '',
        nazwisko: ''
      }
    },
    methods: {
      addNew() {
        if(this.imie.length!=0&&this.nazwisko.length!=0) {
          this.parti.push(this.imie + " " + this.nazwisko);
        }else{
          alert('ani imie ani nazwisko nie może być puste!');
        }
      },
      remove(t) {
        this.parti.indexOf(t, this.i);
        this.parti.splice(this.i, 1);
      }
    }
  };
</script>


<template>
  <div>
    <HeaderAvengerVue />
    <ButtonsAvengersVue :avenger="avenger" @handle-set-avenger="handleSetAvenger"/>
    <MainAvengerVue :avenger="avenger"/>
  </div>
</template>

<script>
import HeaderAvengerVue from './components/HeaderAvenger.vue';
import ButtonsAvengersVue from './components/ButtonsAvengers.vue';
import MainAvengerVue from './components/MainAvenger.vue';

export default {
  name: 'App',
  components: {
    HeaderAvengerVue,
    ButtonsAvengersVue,
    MainAvengerVue,
  },
  data() {
    return {
      avenger: 'Hulk',
    }
  },
  methods: {
    handleSetAvenger: function(name) {
        this.avenger = name
        console.log(this.avenger)
      }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #101010;
}
</style>

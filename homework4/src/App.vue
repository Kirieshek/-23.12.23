<template>
  <div>
    <input v-model="input1" placeholder="Введите текст" />
    <input v-model="input2" placeholder="Введите текст" />
    <button @click="swapText">Обменять тексты</button>
  </div>

  <br>
  <br>
  <br>

  <div>
    <input type="text" v-model="fio" placeholder="ФИО">
    <button @click="splitFio">Получить ФИО</button>
    <p>{{ lastName }}</p>
    <p>{{ firstName }}</p>
    <p>{{ middleName }}</p>
  </div>
</template>

<script>
export default {
  methods: {
      swapText() {
        const temp = this.input1;
        this.input1 = this.input2;
        this.input2 = temp;
      },
      splitFio() {
        const fioArray = this.fio.split(" ");
        this.lastName = fioArray[0];
        this.firstName = fioArray[1];
        this.middleName = fioArray[2];
      } 
    },
  
  computed: {

  },
  data() {
    return {
      input1: '',
      input2: '',
      fio: "",
      lastName: "",
      firstName: "",
      middleName: ""
    }
  },
}
</script>

<style>

</style>

<script>
  export default{
    data(){
      return{
        number1: null,
        number2: null,
        totalResult: null,
      }
    },
    methods:{
      collection(){
        const collect = +this.number1 + +this.number2;
        this.totalResult = collect;
      },
      division(){
        const divis = this.number1 / this.number2;
        this.totalResult = divis;
      },
      extraction(){
        const extra = this.number1 - this.number2;
        this.totalResult = extra;
      },
      multiplication(){
        const multi = this.number1 * this.number2;
        this.totalResult = multi;
      }
    }
  }
</script>

<template>
  <div>
    <v-container class="">
      <p class="text-center">Hesap makinesi</p>
      <p> {{ totalResult > 100 ? "100'den Büyük" : "100'den Küçük" }}</p>

      <h1>{{ totalResult }}</h1>
    <v-text-field v-model="number1"></v-text-field>
    <v-text-field v-model="number2"></v-text-field>
    <div >
    <v-btn class="gap-5" @click="collection">Topla</v-btn>
    <v-btn class="gap-5" @click="extraction">Çıkart</v-btn>
    <v-btn class="gap-5" @click="division">Böl</v-btn>
    <v-btn class="gap-5" @click="multiplication">Çarp</v-btn>
  </div>
  </v-container>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.gap-5{
  margin-right: 5px;
}
.button{
  border: 1px solid black;
  padding: 8px;
}
.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>

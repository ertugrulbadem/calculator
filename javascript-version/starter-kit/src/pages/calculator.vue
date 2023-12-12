<script setup>
const number1 = ref(0)
const number2 = ref(0)
const totalResult = ref(0)

const collection = ()=>{
  totalResult.value = Number(number1.value) + Number(number2.value)
}

const extraction = () =>{
  totalResult.value = Number(number1.value) - Number(number2.value)
}

const division = () =>{
  totalResult.value = Number(number1.value) / Number(number2.value)
}

const multiplication = () =>{
  totalResult.value = Number(number1.value) * Number(number2.value)
}
</script>

<template>
    <div>
        <VCard title="Hesap Makinesi">
            <VCardText>{{ totalResult }}</VCardText>
            <AppTextField label="Number 1" v-model="number1" class="mx-auto"/>
            <AppTextField label="Number 2" v-model="number2" class="mx-auto"/>
            <div class="buttons">
            <VBtn color="primary" @click="collection">Collection</VBtn>
            <VBtn color="primary" @click="extraction">Extraction</VBtn>
            <VBtn color="primary" @click="division">Division</VBtn>
            <VBtn color="primary" @click="multiplication">Multiplication</VBtn>
          </div>
          </VCard>
    </div>
</template>

<style>
.mx-auto{
  width: 45%;
  padding-bottom: 20px;
}
.buttons{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 12px;
}
</style>
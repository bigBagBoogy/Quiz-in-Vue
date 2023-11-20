<script setup>
import q from './data/quizes.json'
import { ref, watch } from 'vue'

const quizes = ref(q)
const search = ref('')

watch(search, () => {
  quizes.value = q.filter(q => q.name.toLowerCase().includes(search.value.toLowerCase()))
})

</script>

<template> 
    <div class=container>
    <header> 
      <div class="h1">quiz</div>
       <input v-model.trim="search" type="text" placeholder="Search...">
    </header> 
      <div class="options-container">
        <!-- <div v-for="quiz in quizes" :key="quiz.id" class="card">
          <img :src="quiz.img">
            <div class="card-text">
              <h2>{{quiz.name}}</h2>
              <p>{{quiz.questions.length}} questions  </p>
            </div>
        </div> -->
      </div>
    </div>
</template>

<style scoped>
.container {
  max-width: 1000px;
  margin: 0 auto;
}
header {
  margin-bottom: 10px;
  margin-top: 30px;
  display: flex;
  align-items: center;
}
header input {
  border-radius: 5px;
  height: 25px;
  margin-left: 10px;
  padding: 5px;
  outline: none;
}
.h1 {
  font-size: 3rem;
  margin-right: 50px;
}

.options-container {
  margin-top: 40px;
  display: grid;
  grid-template-columns: auto auto auto auto;
  gap: 10px;
  padding: 10px;
}



</style>
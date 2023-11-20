<script setup>
import q from './data/quizes.json'
</script>

<template> 
    <div class=container>
      {{ q }}
    <header> 
      <div class="h1">quiz</div>
       <input type="text" placeholder="Search...">
    </header> 
  <div class="options-container"></div>
  <div class="card">
    <img src="https://miro.medium.com/v2/resize:fit:1400/1*L76A5gL6176UbMgn7q4Ybg.jpeg" alt="math">
      <div class="card-text">
        <h2>Math</h2>
        <p>10 questions</p>
      </div>
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
background-color: aqua;
  outline: none;
}
.h1 {
  font-size: 3rem;
  margin-right: 50px;
}

.options-container {
  display: flex;
  flex-wrap: wrap;
  margin-top: 40px;
}
.card {
  max-width: 310px;
  overflow: hidden; 
  border-radius: 2%;
  box-shadow: rgba(0, 0, 0, 0.1);
  margin-bottom: 35px;
  margin-right: 20px;
  cursor: pointer;
}
.card img {
  width: 100%;
  height: 190px;
  margin: 0;
}

.card .card-text {
  padding: 0 5px;
}

.card .card-text h2 {
 font-weight: bold;
}

</style>
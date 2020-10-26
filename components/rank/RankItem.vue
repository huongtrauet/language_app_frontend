<template>
  <div class="card_content flex">
    <div class="flex">
      <img :src="imgsrc" class="ava" alt="" />
      <div class="index">{{ index }}</div>
    </div>
    <div class="name">{{ name }}</div>
    <div class="score">{{ score }}</div>
  </div>
</template>
<script>
export default {
  props: {
    imgsrc: {
      type: String,
      default:
        "https://i.pinimg.com/originals/fa/9d/ec/fa9dec24c7b2ed97960501a74b3feb84.jpg#",
    },
    index: {
      type: Number,
      default: 1,
    },
    name: {
      type: String,
      default: "Huong Tra",
    },
    score: {
      type: Number,
      default: 1000,
    },
  },
};
</script>
<style scoped>
.card_content {
  width: 100%;
  background-color: white;
  margin: 5px 0;
  padding: 5px;
  display: flex;
  font-size: 14px;
}
.flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.ava {
  width: 30px;
  height: 30px;
  margin-right: 5px;
  border-radius: 50%;
}
</style>

<template>
  <div class="card_content">
    <div class="card_img">
      <img
        src="https://i.pinimg.com/originals/fa/9d/ec/fa9dec24c7b2ed97960501a74b3feb84.jpg#"
        alt="ciu ciu"
      />
    </div>
    <div class="card_title">
      <p>{{ lessonname }}</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    lessonname: {
      type: String,
      default: "Memrise lesson",
    },
  },
};
</script>
<style scoped>
.card_content {
  width: 18%;
  background-color: white;
  margin: 5px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 10px;
}

.card_img {
  width: 80%;
  height: 150px;
}

.card_img img {
  width: 100%;
  height: 100%;
}
</style>

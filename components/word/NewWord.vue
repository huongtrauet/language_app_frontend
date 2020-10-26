<template>
  <div class="container">
    <div class="hira">{{ hira }}</div>
    <div class="kanji">{{ kanji }}</div>
    <div class="time">{{ time }}</div>
  </div>
</template>
<style scoped>
.container {
  padding: 0px 1em;
  margin: 1em 0px;
  display: flex;
  justify-content: space-between;
  font-size: 18px !important;
  border-bottom: 1px solid #e4e4e4;
}
.hira {
  width: 40%;
  font-weight: bold;
}
.kanji {
  width: 50%;
}
.time {
  width: 10%;
}
.line {
  border: 1px solid;
}
</style>
<script>
export default {
  props: {
    hira: {
      type: String,
      default: "Hira",
    },
    kanji: {
      type: String,
      default: "Kanji",
    },
    time: {
      type: String,
      default: "Time",
    },
  },
};
</script>

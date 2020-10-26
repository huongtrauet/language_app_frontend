<template>
  <div class="card_content">
    <div class="title">Leaderboard</div>
    <div class="option">
      <div>
        <a-tabs default-active-key="1">
          <a-tab-pane key="1" tab="Week">
            <div v-for="(item, index) in rank_list" :key="index">
              <rank-item
                :index="index"
                :name="item.name"
                :score="item.score"
                :imgsrc="item.imgsrc"
              ></rank-item>
            </div>
          </a-tab-pane>
          <a-tab-pane key="2" tab="Month"> Content of Tab Pane 2 </a-tab-pane>
          <a-tab-pane key="3" tab="Year"> Content of Tab Pane 3 </a-tab-pane>
        </a-tabs>
      </div>
    </div>
  </div>
</template>
<style scoped>
.title {
  text-align: center;
  font-size: 25px;
  font-weight: bold;
  padding-top: 10px;
}
</style>
<script>
import RankItem from "@/components/rank/RankItem.vue";
export default {
  components: {
    "rank-item": RankItem,
  },
  data: function () {
    return {
      rank_list: [
        {
          imgsrc:
            "https://i.pinimg.com/originals/fa/9d/ec/fa9dec24c7b2ed97960501a74b3feb84.jpg#",
          name: "Huong Tra",
          score: 123456,
        },
        {
          imgsrc:
            "https://i.pinimg.com/originals/fa/9d/ec/fa9dec24c7b2ed97960501a74b3feb84.jpg#",
          name: "Huong Tra",
          score: 123456,
        },
        {
          imgsrc:
            "https://i.pinimg.com/originals/fa/9d/ec/fa9dec24c7b2ed97960501a74b3feb84.jpg#",
          name: "Huong Tra",
          score: 123456,
        },
      ],
    };
  },
};
</script>

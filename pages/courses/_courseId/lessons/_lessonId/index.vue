<template>
  <div class="container">
    <div class="info-container">
      <div class="info block">
        <div class="info_left">
          <img
            src="https://i.pinimg.com/originals/fa/9d/ec/fa9dec24c7b2ed97960501a74b3feb84.jpg#"
            alt="ciu ciu"
          />
          <h1 class="course-title">Soumatome N3 Kanji - Hán tự</h1>
        </div>
        <div class="info_right">
          <img
            src="https://i.pinimg.com/originals/fa/9d/ec/fa9dec24c7b2ed97960501a74b3feb84.jpg#"
            alt="ciu ciu"
          />
          <div>Created by</div>
          <div class="created-user-name">Huong Tra</div>
        </div>
      </div>
    </div>
    <div class="level">
      <div class="level-button">
        <button><a-icon type="unordered-list" />&nbsp; Levels(10)</button>
      </div>
      <div class="level-button">
        <button><a-icon type="thunderbolt" />&nbsp;Difficult words</button>
      </div>
    </div>
    <div class="content-container">
      <div class="content">
        <div class="progress">
          <div class="progress-left">
            <img
              src="https://i.pinimg.com/originals/fa/9d/ec/fa9dec24c7b2ed97960501a74b3feb84.jpg#"
              alt="ciu ciu"
            />
          </div>
          <div class="progress-right">
            <div class="progress-des">
              <h1>Tuần 1 - 1</h1>
            </div>
            <div class="progress-bar">
              <a-progress
                :percent="50"
                status="active"
                stroke-color="#ffc000"
              />
            </div>
            <div class="option">
              <div class="option-dropdown">
                <a-dropdown-button class="menu-item">
                  Options
                  <a-menu slot="overlay" class="menu-item">
                    <a-menu-item key="1">
                      <nuxt-link to="/courses">English</nuxt-link>
                    </a-menu-item>
                    <a-menu-item key="2">
                      <nuxt-link to="/courses">Tiếng việt</nuxt-link>
                    </a-menu-item>
                  </a-menu>
                </a-dropdown-button>
              </div>
              <div class="words">
                <button>Review 15 words</button>
              </div>
            </div>
          </div>
        </div>
        <div class="level-view">
          <div>15 words</div>
          <div>0 ignored</div>
        </div>
        <div class="list_lesson">
          <div class="thing-header">
            <div class="thing-header-item">Ready to learn</div>
            <div class="thing-header-item">Ready to review</div>
            <button class="thing-header-item">Ignore</button>
          </div>
          <div class="list-new-word">
            <div v-for="(item, index) in list_words" :key="index">
              <component-new-word-card
                :hira="item.hira"
                :kanji="item.kanji"
                :time="item.time"
              ></component-new-word-card>
            </div>
          </div>
        </div>
        <a class="next-level">Level 2&nbsp;<a-icon type="right" /></a>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
h1,
h3 {
  color: white;
}
.menu-item {
  margin: 0px 1em;
}
.container {
  width: 100%;
  font-size: 14px;
}

.info {
  display: flex;
  background-color: #2b3648;
}
.info-container {
  background-color: #2b3648;
  color: white;
  padding-bottom: 10px;
}

.block {
  width: 50%;
  margin: 0 auto;
}
.info_left {
  width: 80%;
  margin-right: 20px;
  display: flex;
}
.info_left img {
  width: 6%;
  height: 50%;
}
.course-title {
  margin-left: 20px;
}
.info_right {
  width: 20%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.info_right img {
  width: 20%;
}
.created-user-name {
  font-weight: bold;
}
.level-button button {
  border-radius: 30px;
  border: 1px solid white;
  padding: 0.5em 3em;
  margin: 0 1em;
  background-color: white;
  cursor: pointer;
  &:hover {
    background-color: #a7cddc;
  }
}
.progress {
  display: flex;
  margin: 0 2em;
}
.progress-left {
  width: 15%;
  margin-right: 3em;
  padding-bottom: 2em;
}
.progress-left img {
  width: 100%;
  height: 100%;
}
.progress-right {
  width: 85%;
}
.progress-des h1 {
  color: black;
}
.level-view {
  background-color: #fcfaf2;
}
.option {
  display: flex;
  justify-content: space-between;
  margin: 2em 0px;
}
.words button {
  color: #2b3648;
  background-color: #4ead84;
  font-weight: bold;
  padding: 5px 15px;
  border-radius: 10px;
  font-size: 14px;
  border: 1px solid #e4e4e4;
  cursor: pointer;
}
.thing-header {
  display: flex;
  justify-content: flex-end;
}
.thing-header button {
  padding: 5px 10px;
  border-radius: 10px;
  border: 1px solid #e4e4e4;
  cursor: pointer;
}
.thing-header-item {
  margin-left: 6em;
  margin-right: 2em;
}
.level-view {
  display: flex;
  justify-content: space-between;
  padding: 1.2em 2em;
}
.lesson_card {
  display: flex;
  flex-wrap: wrap;
  width: 70%;
}

.description {
  font-size: 16px;
}

.level {
  width: 55%;
  margin: 0 auto;
  padding: 20px 0px;
  display: flex;
}
.content-container {
  background-color: #fcfaf2;
  overflow: auto;
  display: flex;
}
.content {
  padding: 20px 0px;
  background-color: white;
  width: 40%;
  margin: 20px auto;
  position: relative;
}
.next-level {
  position: absolute;
  top: 10%;
  right: -25%;
  color: #2b3648;
  background-color: white;
  width: 20%;
  height: 10%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 20px;
  font-weight: bold;
  border-radius: 10px;
}
.list_lesson {
  display: flex;
  flex-direction: column;
  padding: 1em 0px;
}
.rank {
  width: 30%;
  background-color: white;
}
</style>
<script>
import NewWord from "@/components/word/NewWord.vue";
export default {
  components: {
    "component-new-word-card": NewWord,
  },
  data: function () {
    return {
      list_words: [
        {
          hira: "かんたん",
          kanji: "簡単",
          time: "now",
        },
        {
          hira: "かんたん",
          kanji: "簡単",
          time: "now",
        },
        {
          hira: "かんたん",
          kanji: "簡単",
          time: "now",
        },
        {
          hira: "かんたん",
          kanji: "簡単",
          time: "now",
        },
        {
          hira: "かんたん",
          kanji: "簡単",
          time: "now",
        },
        {
          hira: "かんたん",
          kanji: "簡単",
          time: "now",
        },
        {
          hira: "かんたん",
          kanji: "簡単",
          time: "now",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="info-container">
      <div class="info block">
        <div class="info_left">
          <img
            src="https://i.pinimg.com/originals/fa/9d/ec/fa9dec24c7b2ed97960501a74b3feb84.jpg#"
            alt="ciu ciu"
          />
        </div>
        <div class="info_right">
          <div class="source">Coures > Languages > Japanese > Japanese</div>
          <div class="title">
            <h1>Soumatome N3 HAN TU</h1>
          </div>
          <div class="description" />
          <h1>Welcome to Memrise</h1>
          <h3>
            Join millions of people who are already learning for free on
            Memrise! It’s fast, it’s fun and it’s mind-bogglingly effective
          </h3>
          <div class="start_button">
            <button>Get started now</button>
          </div>
        </div>
      </div>
    </div>
    <div class="level">
      <div class="level-button">
        <button class="active">
          <a-icon type="unordered-list" />&nbsp; Levels(10)
        </button>
      </div>
      <div class="level-button">
        <button><a-icon type="thunderbolt" />&nbsp;Difficult words</button>
      </div>
    </div>
    <div class="content">
      <div class="list_lesson block">
        <div class="lesson_card">
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
                <div class="action">
                  <button><a-icon type="thunderbolt" /> 0</button>
                  <button><a-icon type="clock-circle" /></button>
                  <button>Review(256)</button>
                </div>
              </div>
            </div>
          </div>
          <component-lesson-card lessonname="leasson 1"></component-lesson-card>
          <component-lesson-card lessonname="leasson 2"></component-lesson-card>
          <component-lesson-card lessonname="leasson 3"></component-lesson-card>
          <component-lesson-card lessonname="leasson 4"></component-lesson-card>
          <component-lesson-card lessonname="leasson 5"></component-lesson-card>
          <component-lesson-card lessonname="leasson 6"></component-lesson-card>
          <component-lesson-card lessonname="leasson 7"></component-lesson-card>
          <component-lesson-card lessonname="leasson 8"></component-lesson-card>
        </div>
        <div class="rank">
          <rank></rank>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
h1,
h3 {
  color: white;
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
  width: 55%;
  margin: 0 auto;
}
.info_left {
  width: 40%;
  margin-right: 20px;
}
.info_left img {
  width: 100%;
}

.info_left img {
  width: 100%;
}

.lesson_card {
  display: flex;
  flex-wrap: wrap;
  width: 70%;
}

.description {
  font-size: 16px;
}

.start_button button {
  color: white;
  background-color: #83ca38;
  font-weight: bold;
  padding: 10px 30px;
  border-radius: 10px;
  font-size: 16px;
  margin: 1em 0;
  border: none;
  cursor: pointer;
}
.level {
  width: 55%;
  margin: 0 auto;
  padding: 20px 0px;
}
.content {
  padding: 30px 0px;
  background-color: #fcfaf2;
}
.list_lesson {
  display: flex;
}
.rank {
  width: 30%;
  background-color: white;
}
.progress {
  display: flex;
  width: 100%;
  margin: 0px 18px 20px 3px;
  padding: 20px 20px;
  background-color: white;
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
.option {
  display: flex;
  justify-content: space-between;
  margin: 1em 0;
}
.action button {
  padding: 0.5em;
  border-radius: 8px;
  background-color: #a7cddc;
  border: none;
  cursor: pointer;
}
.level {
  width: 55%;
  margin: 0 auto;
  padding: 20px 0px;
  display: flex;
}
.active {
  background-color: #b9d7e3;
}
.level-button button {
  border-radius: 30px;
  border: 1px solid white;
  padding: 0.5em 3em;
  margin: 0 1em;
  cursor: pointer;
  &:hover {
    background-color: #a7cddc;
  }
}
</style>
<script>
import LessonCard from "@/components/LessonCard.vue";
import Rank from "@/components/rank/Rank.vue";
export default {
  components: {
    "component-lesson-card": LessonCard,
    rank: Rank,
  },
};
</script>

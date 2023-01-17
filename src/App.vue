<template>
  <div class="main-contents">
    <div class="header">
      <div class="main-nav">
        <div class="main-nav-jaem">
          <button class="nav-btn hbg">
            <div class="hbg_line"></div>
            <div class="hbg_line hbg_line_middle"></div>
            <div class="hbg_line"></div>
          </button>
          <a class="main-nav-logo">
            <!-- 로고자리 -->로고에용
          </a>
        </div> 
        <div class="main-nav-jaem">

        </div>
      </div>
    </div>
    

    <button class="bottom-btn left-btn">
      버튼1
    </button>
    <button class="bottom-btn right-btn">
      버튼2
    </button>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
  components: {
    
  },
})

export default class App extends Vue {}
</script>

<style>
body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.main-contents {
  width: 100%;
  height: 100vh;
  background: url("./assets/background_img.jpg") no-repeat center;
  background-size: cover;
}

.contents {
  height:1000px;
  width: 100%;
}

.header {
  width: 100%;
  height: 45px;
  background : 0;
  color : #eee;
  padding-bottom: 8px;
  position: sticky;
  top: 0;
}

.footer {
  width: 100%;
  position: sticky;
  bottom: 0;
  padding-bottom: 10px;
  background-color: white;
}

.main-nav {
    display: flex;
    height: 50px;
    left: 0;
    padding: 0 10px;
    position: absolute;
    top: 0;
    width: 100%;
    z-index: 1000;
    padding : 0;
}

.main-nav-jaem {
  align-items: center;
  display: flex;
  flex: 1 0 0;
}

.main-nav-logo {
  display: block;
  left: 50%;
  position: absolute;
  transform: translate3d(-50%,0,0);
  transition: opacity .5s;
}

.hbg_line {
    background: #bbb;
    border-radius: 5px;
    height: 3px;
    transition: transform .35s var(--ease-in-out-cubic),opacity .35s var(--ease-in-out-cubic);
    width: 20px;
}

.hbg_line_middle {
  margin: 3px 0;
}

.hbg {
  align-items: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  transition: opacity .35s var(--ease-in-out-cubic);
}

.nav-btn {
    height: 40px;
    margin: 5px;
    width: 25px;
}

button {
  background: 0;
  border: 0;
  color: inherit;
  font: inherit;
  outline: 0;
  padding: 0;
  vertical-align: baseline;
  cursor: pointer;
}

.bottom-btn {
  background: var(--masonry-alt);
  bottom: 50vh;
  -webkit-box-shadow: 0 5px 10px 0 rgba(255, 255, 255, 0.3);
  box-shadow: 0 5px 10px 0 rgba(255, 255, 255, 0.3);
  color: #fff;
  font-size: 15px;
  height: 30px;
  line-height: 30px;
  opacity: 1;
  overflow: hidden;
  position: fixed;
  text-align: center;
  transition: opacity .35s;
  width: 30px;
  z-index: 350;
  border-radius: 50%;
}

.left-btn {
  left: 20px;
}

.right-btn {
  right: 20px;
}

</style>

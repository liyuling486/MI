<template>
  <div>

    <div class="header">
      <div class="headerSear">
        <div class="msg"></div>
        <div class="search">
          <i class="searchIcon"></i>
          <input type="text">
        </div>
        <div class="scan"></div>
      </div>

      <div class="tabList">
        <div class="tabUl">
          <div class="tabItem" :class="{ 'act' : index == tabIndex }" v-for="(value, index) in tabList" :key="index" @click="tabChange(index)">
            <span>{{value}}</span>
          </div>
        </div>
      </div>
    </div>

  <div class="con">
    <swiper :list="bannerList"></swiper>

    <div class="type">
      <a href="javascript:;">
        <img src="http://qiniu.verydog.cn//show.liluo.cc/2018011022292984819.png" alt="">
      </a>
      <a href="javascript:;">
        <img src="http://qiniu.verydog.cn//show.liluo.cc/2018011022292372054.png" alt="">
      </a>
      <a href="javascript:;">
        <img src="http://qiniu.verydog.cn//show.liluo.cc/2018011022291629252.png" alt="">
      </a>
      <a href="javascript:;">
        <img src="http://qiniu.verydog.cn//show.liluo.cc/2018011022290460400.png" alt="">
      </a>
    </div>


  </div>




  </div>
</template>

<script>
  import swiper from '../../components/swiper'

  export default {
    name: "index",
    data() {
      return {
        tabIndex: 0,
        tabList: ['推荐', '手机', '智能', '电视', '电脑', '全面屏', '生活周边', '盒子'],
        bannerList : [
          {
            src: 'http://qiniu.verydog.cn//show.liluo.cc/01.png',
            href: '/detail/1001'
          },
          {
            src: 'http://qiniu.verydog.cn//show.liluo.cc/02.jpg',
            href: '/detail/1002'
          },
          {
            src: 'http://qiniu.verydog.cn//show.liluo.cc/03.jpg',
            href: '/detail/1003'
          },
          {
            src: 'http://qiniu.verydog.cn//show.liluo.cc/04.jpg',
            href: '/detail/1004'
          }
        ],
      }
    },
    methods: {
      tabChange: function (index) {
        this.tabIndex = index;
      }
    },
    components: {
      swiper
    }
  }
</script>

<style scoped>
  .header{
    background: #f2f2f2;
    box-shadow: 0 2px 4px -1px rgba(0,0,0,.2);
  }
  .headerSear {
    padding: 0.6rem;
    display: flex;
    justify-content: space-between;
  }

  .search {
    width: 100%;
    height: 1.5rem;
    border: 1px solid #ddd;
    margin: 0 1rem;
  }

  .searchIcon {
    display: inline-block;
    background: #f00;
    width: 1.5rem;
    height: 1.5rem;
  }

  .search input {
    width: 80%;
    background: transparent;
    vertical-align: 0.5rem;
    border: 0;
    outline: none;
  }

  .msg, .scan {
    width: 2rem;
    height: 2rem;
    background: #f00;
  }

  .tabList {
    overflow-x: auto;
  }

  .tabUl {
    width: auto;
    white-space: nowrap;
  }

  .tabItem {
    display: inline-block;
    padding: 0 0.3rem;
    line-height: 2rem;
  }
  .tabItem.act{
    border-bottom: 1px solid #f00;
  }
  .type {
    display: flex;
  }
  .type img {
    width: 100%;
  }

</style>

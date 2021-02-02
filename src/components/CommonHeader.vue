<template>
  
    <div id="firstview">
      <header id="top-header">
        <div class="flex">
          <h1 class="header-logo">estra inc.</h1>
          <nav class="header-nav">
            <ul>
              <li><a href="#">home</a></li>
              <li><a href="#">about</a></li>
              <li><a href="#">service</a></li>
              <li><a href="#">works</a></li>
              <li><a href="#">price</a></li>
              <li><a href="#">contact</a></li>
            </ul>
          </nav>
        </div>
      </header>
      <p class="catchcopy">機械ではできない仕事を</p>
      <div class="news flex">
        <div class="news-content">
          <p class="news_date">2019/01/01</p>
          <p class="news_title">
            ニュースタイトルがここには入ります。3月の決算報告書
          </p>
        </div>
        <div class="news-icon">news</div>
      </div>
    

            
      
    <div id="hamburger" @click="hamburger()" v-bind:class="{'active' :isClass}">
      <span></span>
      <span></span>
      <span></span>
    </div>

      <nav class="menu-content" :class="{'open':isClass}">
      <p class="menu-title">estra inc.</p>
      <ul class="menu-content_inner">
        <li>
          <a href="#">home</a>
        </li>
        <li>
          <a href="#">about</a>
        </li>
        <li>
          <a href="#">service</a>
        </li>
        <li>
          <a href="#">works</a>
        </li>
        <li>
          <a href="#">price</a>
        </li>
        <li>
          <a href="#">contact</a>
        </li>
      </ul>
    </nav>


  </div>


  
</template>

<script>
export default {
  data() {
    return {
      isClass: false
    };
  },
  methods: {
    hamburger() {
      this.isClass = !this.isClass; //trueとfalseを切り替え
    }
  }
};
</script>

<style scoped>

.menu-content {
  display: none;
}

#hamburger {
  display: none;
}

#top-header {
  height: 70px;
  line-height: 70px;
  background: rgba(0, 0, 0, 1);
}

.header-logo {
  font-size: 20px;
  font-weight: bold;
  margin-left: 35px;
  color: #fff;
  line-height: 70px;
}

.header-nav li {
  display: inline-block;
  margin-right: 35px;
  font-size: 16px;
}

.header-nav a {
  color: #fff;
}

#firstview {
  height: 100vh;
  background: url("~@/assets/img/eyecatch.jpg") no-repeat;
  background-size: cover;
  background-position: center;
  position: relative;
}

/* =====================レスポンシブ=================== */



@media screen and (max-width: 768px) {
  .header-nav {
    display: none;
  }
  
  #hamburger {
    width: 50px;
    height: 40px;
    position: absolute;
    cursor: pointer;
    z-index: 100;
    top: 10px;
    right: 20px;
    transition: 0.1s;
    display: block;
  }
  #hamburger span {
    display: block;
    width: 35px;
    height: 2px;
    background-color: rgb(185, 53, 202);
    transition: 0.1s;
  }
  #hamburger span:nth-of-type(1) {
    position: absolute;
    top: 10px;
    left: 2px;
  }
  #hamburger span:nth-of-type(2) {
    position: absolute;
    top: 20px;
    left: 2px;
  }
  #hamburger span:nth-of-type(3) {
    position: absolute;
    top: 30px;
    left: 2px;
  }

  #hamburger.active span:nth-of-type(1) {
    top: 20px;
    transform: rotate(45deg);
  }

  #hamburger.active span:nth-of-type(2) {
    opacity: 0;
  }
  #hamburger.active span:nth-of-type(3) {
    top: 20px;
    transform: rotate(-45deg)
  }
  .menu-content {
    display: block;
    width: calc(100% - 80px);
    height: 80%;
    text-align: center;
    transition: 0.5s;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    background: rgb(239, 250, 252);
    color: #000;
    box-shadow: 80px 0 rgba(41, 159, 163, 0.3);
    z-index: 999;
  }
  .menu-content .menu-title {
    margin: 40px 20px;
    font-size: 2.2rem;
    color: #000;
    text-align: center;
    font-weight: bold;
  }
  .menu-content li a {
    color: #000;
    margin: 15px;
    padding: 5px;
    border-bottom: 0.5px solid #191e4d;
    text-decoration: none;
    display: block;
  }
  .menu-content li {
    text-align: center;
    width: 100%;
  }
  .menu-content.open {
    left: 0;
  }
}

</style>
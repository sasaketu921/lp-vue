<template>
  <footer class="top-header">
        <div class="header-bar">
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
        </div>
        <small>Copyright 2019 estra inc. All Rights Reserved.</small>
      </footer>
</template>

<style scoped>
.header-bar {
  height: 70px;
  line-height: 70px;
}

.top-header {
  background: #000;
  text-align: center;
  
}

.top-footer small {
  text-align: center;
  color: #fff;
}

.footer-bar ul {
  display: flex;
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

/* ============レスポンシブ=================== */

@media screen and (max-width: 768px) {
.top-footer .header-logo {
    margin: 0;
    width: 100%;
    text-align: center;
  }
}
</style>
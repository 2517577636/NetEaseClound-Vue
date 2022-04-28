<template>
  <div id="app">
    <header>
      <div class="header-content df justify-between">
        <!-- ---------- header left start ---------- -->
        <div class="header-left df">
          <div class="logo pointer">
            <a class="fs-0 db" href="/">网易云音乐</a>
          </div>
          <div class="df fs-14">
            <router-link class="h-c-item discover" to="/">发现音乐</router-link>
            <router-link class="h-c-item my" to="/my">我的音乐</router-link>
            <router-link class="h-c-item focus" to="/focus">关注</router-link>
          </div>
        </div>
        <!-- ---------- header left end ---------- -->
      
        <!-- ---------- header right start ---------- -->
        <div class="header-right df align-center justify-between">
          <div class="searchbar mr-sm">
            <searchBar placeholder="音乐/视频/电台/用户"></searchBar>
          </div>
          
          <div class="login fs-14 pointer">登录</div>
        </div>
        <!-- ---------- header right start ---------- -->
      </div>
      <div class="header-red-bar">
        <div class="header-red-bar-content">
          <navList></navList>
        </div>
      </div>
    </header>
    <router-view/>
  </div>
</template>

<script>
import searchBar from "@/components/searchBar/index.vue"
import navList from "@/components/navlist/index.vue"

export default {
  name: "App",
  components: {
    searchBar,
    navList
  }
}
</script>

<style>
header{
  /* height: var(--header-height); */
  background-color: var(--theme-primary);
}

/* ---- logo start ---- */
.logo {
  height: var(--header-height);
  width: 176px;
  background-image: url("./assets/topbar.png");
}

.logo a {
  height: var(--header-height);
  width: 100%;
}
/* ---- logo end ---- */

/* -------------- header-content start ------------- */
.header-content {
  height: var(--header-height);
  width: 80%;
  margin: 0px auto;
}

.h-c-item {
  height: var(--header-height);
  padding: 0 19px;
  line-height: var(--header-height);
  color: var(--text-color-gray);
}

.h-c-item:hover {
  background-color: var(--bg-black);
  color: var(--text-color-white);
}

.router-link-exact-active {
  background-color: var(--bg-black);
  color: var(--text-color-white);
}
/* -------------- header-content end ------------- */

/* -------------- header-read start ------------- */
.header-red-bar {
  height: 0.5rem;
  background-color: var(--bg-red);
}

.header-red-bar-content {
  width: 80%;
  height: inherit;
  margin: 0 auto;
}
/* -------------- header-read end ------------- */
</style>

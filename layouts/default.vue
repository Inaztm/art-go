<template>
  <div class="big-wrapper">
    <div class="banner-image"></div>
    <main class="page">
      <nav class="navigation">
        <section class="space-x space-top space-bottom-sm">
          <a class="flex --center-items" href="#">
            <i class="site-inc --space"></i>
            <div>
              <h3>ArtGo portfolio</h3>
              <p>By Siyanchuk Nazar</p>
            </div>
          </a>
        </section>
        <section class="navigation__scroll-flex">
          <div class="list">
            <nuxt-link
              :to="{ name: 'collections' }"
              active-class="--active"
              class="list__link">
              <i class="mi mi-AllApps space-right-sm"></i>
              <span>Коллекции</span>
            </nuxt-link>
            <nuxt-link
              :to="{ name: 'order' }"
              active-class="--active"
              class="list__link">
              <i class="mi mi-Send space-right-sm"></i>
              <span>Заказать работу</span>
            </nuxt-link>
            <nuxt-link
              :to="{ name: 'about' }"
              active-class="--active"
              class="list__link">
              <i class="mi mi-Accounts space-right-sm"></i>
              <span>Обо мне</span>
            </nuxt-link>
          </div>
        </section>
        <section class="space-y">
          <div class="list">
            <nuxt-link
              :to="{ name: 'settings' }"
              active-class="--active"
              class="list__link">
              <i class="mi mi-Settings space-right-sm"></i>
              <span>Настройки</span>
            </nuxt-link>
          </div>
        </section>
      </nav>
      <section class="content">
        <nuxt />
      </section>
    </main>
  </div>
</template>

<style>
@import url("../assets/micon/css/micon.css");

@font-face {
  font-family: 'lato-regular';
  src: url("/assets/lato-font/Lato-Regular.ttf") format("truetype");
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'lato-semibold';
  src: url("/assets/lato-font/Lato-Semibold.ttf") format("truetype");
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: 'lato-light';
  src: url("/assets/lato-font/Lato-Light.ttf") format("truetype");
  font-weight: normal;
  font-style: normal;
}

*,
*:before,
*:after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.big-wrapper {
  position: relative;
  display: flex;
  flex-direction: column;
  height: 100vh;
  font-family: "lato-regular";
}
.banner-image {
  z-index: -1;
  position: fixed;
  left: 0;
  top: 0;
  background-color: #333;
  background-image: url("/assets/images/cover.jpg");
  background-size: cover;
  opacity: .5;
  width: 100vw;
  height: 100vh;
}
h4 {
  font-weight: medium;
}
a {
  color: #333;
  text-decoration: none;
}
b {
  font-family: "lato-semibold";
}
.flex {
  display: flex;
}
.flex.--center {
  text-align: center;
}
.flex.--center-items {
  align-items: center;
}
.space {
  margin: 35px;
}
.space-sm {
  margin: 15px;
}
.space-mm {
  margin: 8px;
}
.space-x {
  margin-left: 35px;
  margin-right: 35px;
}
.space-x-sm {
  margin-left: 15px;
  margin-right: 15px;
}
.space-x-mm {
  margin-left: 8px;
  margin-right: 8px;
}
.space-y {
  margin-top: 35px;
  margin-bottom: 35px;
}
.space-y-sm {
  margin-top: 15px;
  margin-bottom: 15px;
}
.space-y-mm {
  margin-top: 8px;
  margin-bottom: 8px;
}
.space-top {
  margin-top: 35px;
}
.space-top-sm {
  margin-top: 15px;
}
.space-top-mm {
  margin-top: 8px;
}
.space-bottom {
  margin-bottom: 35px;
}
.space-bottom-sm {
  margin-bottom: 15px;
}
.space-bottom-mm {
  margin-bottom: 8px;
}
.space-left {
  margin-left: 35px;
}
.space-left-sm {
  margin-left: 15px;
}
.space-left-mm {
  margin-left: 8px;
}
.space-right {
  margin-right: 35px;
}
.space-right-sm {
  margin-right: 15px;
}
.space-right-mm {
  margin-right: 8px;
}
.site-inc {
  display: inline-block;
  width: 31px;
  height: 31px;
  background-image: url("/assets/images/logo.svg");
  background-size: 100%;
}
.site-inc.--space {
  margin-right: 15px;
}
.page {
  display: flex;
  overflow: hidden;
  height: 100%;
  margin: 15px 35px;
  border-radius: 8px;
  /* box-shadow: 0px 1px 3px rgba(0,0,0,0.13); */
}
.navigation {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 307px;
  height: 100%;
  background-color: rgba(245,245,245,0.804);
}
.navigation__scroll-flex {
  overflow: auto;
}
.content {
  overflow: auto;
  flex: 1;
  padding: 35px;
  background-color: #fff;
}
.list {
  display: block;
}
.list__link {
  display: flex;
  align-items: center;
  padding: 15px 35px;
  color: #777;
}
.list__link:hover,
.list__link.--active {
  color: #333;
}
.list__link.--active {
  position: relative;
}
.list__link.--active:before {
  content: "";
  z-index: 1111;
  position: absolute;
  left: 0px;
  top: 50%;
  transform: translateY(-50%);
  height: 37%;
  width: 5px;
  background-color: #333;
  border-radius: 0 3px 3px 0;
  animation: scale_birk 1.7s linear infinite;
}
.list.--big-space {
  padding-top: 35px;
  padding-bottom: 35px;
}
@-moz-keyframes scale_birk {
  0% {
    height: 37%;
    width: 5px;
  }
  27% {
    height: 57%;
    width: 1px;
  }
}
@-webkit-keyframes scale_birk {
  0% {
    height: 37%;
    width: 5px;
  }
  27% {
    height: 57%;
    width: 1px;
  }
}
@-o-keyframes scale_birk {
  0% {
    height: 37%;
    width: 5px;
  }
  27% {
    height: 57%;
    width: 1px;
  }
}
@keyframes scale_birk {
  0% {
    height: 37%;
    width: 5px;
  }
  27% {
    height: 57%;
    width: 1px;
  }
}
.titles {
  display: block;
}
.titles__big {
  font-size: 25px;
  color: #333;
}
.titles__big.--sm {
  font-size: 21px;
}
.titles__small {
  font-size: 18px;
  color: #555;
}
.titles__small.--sm {
  font-size: 15px;
}
.titles.--action {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}
.collection {
  display: flex;
  align-items: center;
  margin-bottom: 35px;
}
.collection__image {
  width: 25%;
  height: 178px;
  margin-right: 15px;
  background-color: #f5f5f5;
  border-radius: 8px;
}
.collection__image:last-child {
  margin-right: 0;
}
.collection__image.--sm {
  height: 75px;
}
.collection__images {
  flex: 1;
  display: flex;
  margin-left: 35px;
}
.collection__images.--wrap {
  flex-wrap: wrap;
  margin-left: 0;
}
.collection__images.--wrap .collection__image {
  width: 23.17%;
  margin-bottom: 15px;
}
.collection__space {
  margin-right: 15px;
}
</style>

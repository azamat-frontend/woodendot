<template>
  <div class="navbar">
    <div class="container">
      <div class="row">
        <div class="col-md-3 col-6">
          <div class="logo">
            <router-link class="logo__link" :to="{ name: 'home' }">
              <i></i>
              Woodendot
              <span>Architecture</span>
            </router-link>
          </div>
        </div>
        <div class="col-md-9 col-lg-6 col-6 menu-container">
          <i
            class="menu-toggle"
            :class="{ 'menu-toggle_active': menuIcon }"
            @click="menuToggle"
          ></i>
          <ul class="top-menu" :class="{ 'top-menu_active': menuIcon }">
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'home' }"
                >Главная</router-link
              >
            </li>
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'projects' }"
                >Проекты</router-link
              >
            </li>
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'services' }"
                >Услуги</router-link
              >
            </li>
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'blog' }"
                >Блог</router-link
              >
            </li>
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'company' }"
                >Компания</router-link
              >
            </li>
          </ul>
        </div>
        <div class="col-md-3 d-none d-lg-block nav-social-wrap">
          <div class="nav-social">
            <a class="nav-social__item" href="#" target="_blank">
              <svg xmlns="http://www.w3.org/2000/svg" width="192" height="192" fill="#e3d9d9" viewBox="0 0 256 256"><rect width="256" height="256" fill="none"></rect><circle cx="128" cy="128" r="32"></circle><path d="M172,28H84A56,56,0,0,0,28,84v88a56,56,0,0,0,56,56h88a56,56,0,0,0,56-56V84A56,56,0,0,0,172,28ZM128,176a48,48,0,1,1,48-48A48,48,0,0,1,128,176Zm52-88a12,12,0,1,1,12-12A12,12,0,0,1,180,88Z"></path></svg>
            </a>
            <a class="nav-social__item" href="#" target="_blank">
              <svg xmlns="http://www.w3.org/2000/svg" width="192" height="192" fill="#e3d9d9" viewBox="0 0 256 256"><rect width="256" height="256" fill="none"></rect><path d="M231.3,31.7A16.1,16.1,0,0,0,215,29L30.4,101.5a15.8,15.8,0,0,0-10.1,16.3,16,16,0,0,0,12.8,14.3L80,141.4V200a16,16,0,0,0,9.9,14.8A16.6,16.6,0,0,0,96,216a15.8,15.8,0,0,0,11.3-4.7l26-25.9L172.6,220a16,16,0,0,0,10.5,4,14.2,14.2,0,0,0,5-.8,15.9,15.9,0,0,0,10.7-11.6L236.4,47.4A16,16,0,0,0,231.3,31.7ZM183.2,208l-82.4-72.5L219.5,49.8Z"></path></svg>
            </a>
            <a class="nav-social__item" href="#" target="_blank">
              <svg xmlns="http://www.w3.org/2000/svg" width="192" height="192" fill="#e3d9d9" viewBox="0 0 256 256"><rect width="256" height="256" fill="none"></rect><path d="M232,128a104.3,104.3,0,0,1-91.5,103.3,4.1,4.1,0,0,1-4.5-4V152h24a8,8,0,0,0,8-8.5,8.2,8.2,0,0,0-8.3-7.5H136V112a16,16,0,0,1,16-16h16a8,8,0,0,0,8-8.5,8.2,8.2,0,0,0-8.3-7.5H152a32,32,0,0,0-32,32v24H96a8,8,0,0,0-8,8.5,8.2,8.2,0,0,0,8.3,7.5H120v75.3a4,4,0,0,1-4.4,4C62.8,224.9,22,179,24.1,124.1A104,104,0,0,1,232,128Z"></path></svg>
            </a>
            <a class="nav-social__item" href="#" target="_blank">
              <svg xmlns="http://www.w3.org/2000/svg" width="192" height="192" fill="#e3d9d9" viewBox="0 0 256 256"><rect width="256" height="256" fill="none"></rect><path d="M245.7,77.7l-30.2,30.1C209.5,177.7,150.5,232,80,232c-14.5,0-26.5-2.3-35.6-6.8-7.3-3.7-10.3-7.6-11.1-8.8a8,8,0,0,1,3.9-11.9c.2-.1,23.8-9.1,39.1-26.4a108.6,108.6,0,0,1-24.7-24.4c-13.7-18.6-28.2-50.9-19.5-99.1a8.1,8.1,0,0,1,5.5-6.2,8,8,0,0,1,8.1,1.9c.3.4,33.6,33.2,74.3,43.8V88a48.3,48.3,0,0,1,48.6-48,48.2,48.2,0,0,1,41,24H240a8,8,0,0,1,7.4,4.9A8.4,8.4,0,0,1,245.7,77.7Z"></path></svg>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView',
  data() {
    return {
      menuIcon: false
    }
  },
  methods: {
    menuToggle() {
      this.menuIcon = !this.menuIcon
    }
  }
}
</script>

<style></style>

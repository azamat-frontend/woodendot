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
					<i class="menu-toggle" :class="{ 'menu-toggle_active': menuIcon }" @click="menuToggle"></i>
          <ul class="top-menu" :class="{ 'top-menu_active': menuIcon }">
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'home' }">Главная</router-link>
            </li>
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'projects' }">Проекты</router-link>
            </li>
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'services' }">Услуги</router-link>
            </li>
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'blog' }">Блог</router-link>
            </li>
            <li class="top-menu__item">
              <router-link class="top-menu__link" :to="{ name: 'company' }">Компания</router-link>
            </li>
          </ul>
        </div>
        <div class="col-md-3 d-none d-lg-block nav-social-wrap">
					<div class="nav-social">
						<a class="nav-social__item" href="#" target="_blank">
							<img src="@/assets/images/interface/fa-soc/instagram-brands.svg" alt="Instagram" />
						</a>
						<a class="nav-social__item" href="#" target="_blank">
							<img src="@/assets/images/interface/fa-soc/vk.svg" alt="VK" />
						</a>
						<a class="nav-social__item" href="#" target="_blank">
							<img src="@/assets/images/interface/fa-soc/facebook-brands.svg" alt="Facebook" />
						</a>
						<a class="nav-social__item" href="#" target="_blank">
							<img src="@/assets/images/interface/fa-soc/twitter-brands.svg" alt="Twitter" />
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

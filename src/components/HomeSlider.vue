<template>
  <div class="home-slider">
    <swiper :navigation="true" :modules="modules" :speed="800" :effect="'fade'" :centeredSlides="true" class="mySwiper">
      <swiper-slide class="home-slider__slide">
				<div class="container">
					<h2 data-animate="bottom" class="home-slider__heading">Woodhouse<br /><span>дизайн на высоком уровне</span></h2>
					<p data-animate="bottom" class="home-slider__text">Разработка и реализация красивых интерьеров из дерева ещё никогда не была так доступна. Интерьеры из дерева различной породы сделают ваш дом уютным и тёплым, радуя вас и ваших гостей.</p>
				</div>
			</swiper-slide>
			<swiper-slide class="home-slider__slide">
				<div class="container">
					<h2 data-animate="bottom" class="home-slider__heading">Деревянные<br /><span>инсталляции любой сложности</span></h2>
					<p data-animate="bottom" class="home-slider__text">Разработка и реализация красивых интерьеров из дерева ещё никогда не была так доступна. Интерьеры из дерева различной породы сделают ваш дом уютным и тёплым, радуя вас и ваших гостей.</p>
				</div>
			</swiper-slide>
			<swiper-slide class="home-slider__slide">
				<div class="container">
					<h2 data-animate="bottom" class="home-slider__heading">Интерьер<br /><span>в современном стиле</span></h2>
					<p data-animate="bottom" class="home-slider__text">Разработка и реализация красивых интерьеров из дерева ещё никогда не была так доступна. Интерьеры из дерева различной породы сделают ваш дом уютным и тёплым, радуя вас и ваших гостей.</p>
				</div>
			</swiper-slide>

			<div class="row home-slider__bottom"></div>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import "swiper/css/effect-fade";
import 'swiper/css/navigation'
import { EffectFade, Navigation } from 'swiper'
export default {
  name: 'HomeSlider',
  components: {
    Swiper,
    SwiperSlide
  },
	data() {
		return {
			modules: [EffectFade, Navigation]
		}
	}
}
</script>

<style scoped lang="scss">
.swiper {
  width: 100%;
  height: 100%;
}

.home-slider {
  position: relative;
  height: 100vh;
  min-height: 580px;
  max-height: 720px;
  color: #fff;
  background-color: var(--dark);
}
.home-slider__slide {
	background-repeat: no-repeat;
  background-size: cover;
	background-position: center;
  display: flex;
  align-items: center;
  padding: 0 10px;
}
.home-slider__slide:nth-child(1) {
	background-image: url('@/assets/images/portfolio/interior-tiel-1.jpg');
}
.home-slider__slide:nth-child(2) {
	background-image: url('@/assets/images/portfolio/interior-tiel-2.jpg');
}
.home-slider__slide:nth-child(3) {
	background-image: url('@/assets/images/portfolio/interior-tiel-3.jpg');
}
.home-slider__slide::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: var(--dark);
  opacity: 0.15;
}
.home-slider__slide::after {
  content: '';
  position: absolute;
  top: 10px;
  right: 10px;
  left: 10px;
  bottom: 10px;
  z-index: 1;
  box-shadow: 0 0 0 30px var(--dark);
  border-radius: var(--radius);
}
.home-slider__slide .container {
  z-index: 2;
  position: relative;
}
[data-animate] {
  opacity: 0;
  transition: all 0.8s ease-out;
}
[data-animate='bottom'] {
  transform: translate3d(0, 15px, 0);
}
.home-slider__slide.swiper-slide-active [data-animate] {
  opacity: 1;
  transform: none;
}
.home-slider__slide.swiper-slide-active .home-slider__heading {
  transition-delay: 0.6s;
}
.home-slider__slide.swiper-slide-active .home-slider__text {
  transition-delay: 1s;
}
.home-slider__heading {
  font-size: 58px;
  line-height: 0.8;
  font-weight: 300;
  margin-bottom: 35px;
  transition-delay: 0.3s;
}
.home-slider__heading span {
  font-size: 16px;
  background-color: var(--accent);
  border-radius: var(--radius-style);
  padding: 6px 16px 7px;
  font-weight: 500;
}
.home-slider__text {
  max-width: 440px;
  font-size: var(--small-text);
  background-color: rgba(32, 35, 40, 0.9);
  padding: 15px 22px;
  border-radius: 0 calc(var(--radius) * 2);
}
.home-slider__bottom {
  position: absolute;
  bottom: 0;
  width: 100%;
  max-width: 440px;
  background-color: var(--dark);
  z-index: 1;
  right: 0;
  border-radius: calc(var(--radius) * 2) 0 0 0;
  padding: 45px 40px 45px 15px;
  font-size: 12px;
  color: #59606c;
}
.home-slider__pagination-wrapper {
  position: relative;
}
.home-slider__pagination {
  font-family: roboto-wt, sans-serif;
  font-weight: 300;
  bottom: inherit;
  margin-top: -10px;
}
.home-slider__pagination span {
  width: 1px;
  height: 28px;
  background-color: #353941;
  display: inline-block;
  vertical-align: middle;
  margin: -3px 8px 0;
}
.home-slider__pagination b {
  position: relative;
  font-size: 15px;
  color: #818b9d;
  font-weight: 300;
}
.home-slider__bottom .swiper-scrollbar-drag {
  height: 5px;
}
.home-slider__nav {
  position: relative;
}
.home-slider__prev,
.home-slider__next {
  outline: none;
}
.home-slider__prev::after,
.home-slider__next::after {
  font-size: 14px;
  color: #818b9d;
}
</style>

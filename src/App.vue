<template>
  <home-header></home-header>
  <router-view />
</template>

<script>
import HomeHeader from '@/components/HomeHeader'

export default {
  name: 'App',
	components: {
		HomeHeader
	}
}
</script>

<style lang="scss"></style>

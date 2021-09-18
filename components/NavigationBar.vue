<template>
  <el-menu :default-active="'Home'" class="nav-menu" mode="horizontal">
    <el-menu-item index="Home">
      صفحه‌ی اصلی
    </el-menu-item>
    <el-menu-item index="2">
      <el-submenu index="2-4">
        <template slot="title">
          <NuxtLink to="/products">
            محصولات
          </NuxtLink>
        </template>
        <el-menu-item index="2-4-1">
          <NuxtLink to="/products/clocks">
            ساعت‌ها
          </NuxtLink>
        </el-menu-item>
        <el-menu-item index="2-4-2">
          item two
        </el-menu-item>
        <el-menu-item index="2-4-3">
          item three
        </el-menu-item>
      </el-submenu>
    </el-menu-item>
    <el-menu-item index="6" class="left-item">
      تست اول
    </el-menu-item>
    <el-menu-item index="5" class="left-item">
      تست دوم
    </el-menu-item>
  </el-menu>
</template>

<script>
export default {
  name: 'NavigationBar',
  data () {
    return {
    }
  },
  computed: {
    currentPathName () {
      return this.$route.name
    },
    activeIndex () {
      switch (this.currentPathName) {
        case 'Main':
          return '1'
        case 'Problems':
        case 'Description':
          return '2'
        case 'Scoreboard':
          return '3'
        case 'Status':
          return '4'
        case 'Judge':
          return '5'
        case 'Admin':
          return '6'
        case 'Login':
          return '10'
        default:
          return '20'
      }
    }
  },
  methods: {
  }
}
</script>

<style lang="css" scoped>
.nav-menu {
  direction: ltr;
}

.nav-menu li:lang(fa) {
  float: right;
}

.nav-menu li.left-item:lang(fa) {
  float: left;
}
</style>

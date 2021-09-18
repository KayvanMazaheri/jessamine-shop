<template>
  <el-container id="app">
    <el-header>
      <NavigationBar />
    </el-header>
    <el-main id="app-inside">
      <Nuxt />
    </el-main>
    <el-footer height="max-content">
      <Footer />
    </el-footer>
  </el-container>
</template>

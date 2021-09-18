<template>
  <p> {{ product }} </p>
</template>

<script>
export default {
  asyncData (ctx) {
    return {
      product: ctx.params.id
    }
  }
}
</script>

<style scoped>

</style>

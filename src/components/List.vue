<template>
  <ul>
    <Item v-for="i in 10" :key="i"/>
  </ul>
</template>

<script>
import Item from './Item.vue'
export default {
  components:{Item}
}
</script>
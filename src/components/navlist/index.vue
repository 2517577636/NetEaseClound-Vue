<template>
  <div class="list">
    <div class="list-item" :class="direction" v-for="(item, idx) in list" :key="idx">
        <div class="l-i-main" :class="[themeType, bgColor]">
            <i class="icon" :class="item.iconName"></i>
            <div class="l-i-main-content">{{item.text}}</div>
            <slot name="markup"></slot>
        </div>
        <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'navList',
  props: {
    list: {
        type: Array,
    },
    bgColor: String,
    themeType: String,
    direction: String
  }
}
</script>

<style scoped>

</style>

<template>
  <div class="search-bar df">
    <i class="db icon" :class="iconName"></i>
    <input 
        class="search-input" 
        :class="placeholderColor" 
        type="text" 
        :name="name" 
        v-model="value" 
        :placeholder="placeholder" 
        @keyup.enter="enterHandler"
    >
  </div>
</template>

<script>
export default {
  name: 'searchBar',
  props: {
    iconName: String,
    placeholder: String,
    placeholderColor: String,
    name: String
  },
  data() {
      return {
          value: ""
      }
  },
  methods: {
    enterHandler() { // 处理提交内容
        this.$emit("search", this.value);
    }
  }
}
</script>

<style scoped>
.search-bar {
    width: 100%;
    height: 32px;
    background-color: var(--bg-white);
    border-radius: var(--radius-sm);
}

.search-input {
    height: inherit;
    padding: 1rem .75rem;
    outline-style: none;
    border: none;
    border-radius: var(--radius-sm);
}

</style>

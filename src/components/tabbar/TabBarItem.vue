<template>
  <div class="tab-bar-item" :class="{active: isActive}">
    <div @click="itemClick">
      <slot name="item-text"></slot>
    </div>

  </div>
</template>

<script>
export default {
  name: "TabBarItem",
  props: {
    link: String
  },
  methods: {
    itemClick() {
      this.$router.replace(this.link)
    }
  },
  computed: {
    isActive() {
      return this.$route.path.indexOf(this.link) !== -1
    }
  }
}
</script>

<style scoped>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 23px;
}

div {
  color: #000000;
  font-family: 微软雅黑;
}

.active {
  background-color: #0bffa8;
}
</style>
<template>
  <div class="nav-button">
    <a href="#">
      <template v-if="this.reversed">
        <slot></slot>
        <material-icon :name="this.icon"></material-icon>
      </template>
      <template v-else>
        <material-icon :name="this.icon"></material-icon>
        <slot></slot>
      </template>
    </a>
  </div>
</template>

<script>
export default {
  name: 'NavButton',
  props: ['icon', 'reversed']
}
</script>

<style scoped lang="scss">

</style>

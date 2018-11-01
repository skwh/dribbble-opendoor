<template>
  <a href="#" :class="{selected: selected, navButton: true}">
    <template v-if="this.reversed">
      <slot></slot>
      <material-icon v-if="this.icon" :name="this.icon" size="26px"></material-icon>
    </template>
    <template v-else>
      <material-icon v-if="this.icon" :name="this.icon" size="26px"></material-icon>
      <slot></slot>
    </template>
  </a>
</template>

<script>
export default {
  name: 'NavButton',
  props: ['icon', 'reversed', 'selected']
}
</script>

<style scoped lang="scss">
@import '../../styles/variables';

.navButton {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin: 1rem 0rem;
  border-radius: 30px;
  padding: 0.1rem 0.8rem;
  font-size: 16px;
  color: $grey;
  transition: background-color 0.25s;

  i {
    margin: 0.7rem;
  }

  &.selected {
    background-color: $highlight;
  }

  &:hover {
    background-color: $highlight;
  }
}
</style>

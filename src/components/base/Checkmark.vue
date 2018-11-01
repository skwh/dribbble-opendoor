<template>
  <div class="checkmark" :class="{filled: checked}">
    <material-icon ng-if="checked" name="check"></material-icon>
  </div>
</template>

<script>
export default {
  name: 'Checkmark',
  props: ['checked']
}
</script>

<style scoped lang="scss">

</style>

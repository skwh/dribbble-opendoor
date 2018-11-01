<template>
  <i class="material-icons" :style="`font-size:${size}`">
    {{ name }}
  </i>
</template>

<script>
export default {
  name: 'MaterialIcon',
  props: ['name', 'size']
}
</script>

<style lang="scss">
i.material-icons {
  vertical-align: sub;
  font-size: inherit;
}
</style>

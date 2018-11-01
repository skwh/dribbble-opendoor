<template>
  <div class="card">
    <div class="card-header">
      <h2 class="title">{{ title }}</h2>
      <p ng-if="action">
        <a :href="action.href">
          {{ action.text }}
        </a>
      </p>
    </div>
    <slot>
    </slot>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: ['title', 'action']
}
</script>

<style scoped lang="scss">

</style>

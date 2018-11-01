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
@import '../../styles/variables';

.card {
  background-color: white;
  border-radius: 10px;
  padding: 1rem 1.5rem;
  color: $grey;
  box-shadow: 1px 1px 1px $light-grey, 0px 0px 1px $light-grey;
  margin-bottom: 2vh;

  .card-header {
    display: flex;
    align-items: center;
    justify-content: space-between;

    .title {
      font-weight: 500;
      color: black;
      margin-bottom: 0.5rem;
    }

    a {
      color: $blue;
      font-size: 0.75rem;
    }
  }
}
</style>

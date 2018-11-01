<template>
  <header>
    <a class="logo" href="#">Opendoor</a>
    <div class="user">
      Nikunj
      <material-icon name="keyboard_arrow_down"
                     size="24px"></material-icon>
    </div>
  </header>
</template>

<script>
export default {
  name: 'opendoor-header'
}
</script>

<style scoped lang="scss">
@import '../styles/variables';

header {
  background-color: white;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
  grid-column-start: 1;
  grid-column-end: 8;
  box-shadow: 1px 1px 5px $highlight;

  .logo {
    font-family: "Playfair Display", serif;
    color: $blue;
    font-size: 1.5rem;
  }

  .user {
    position: relative;

    i {
      position: relative;
      top: 0.5vh;
      color: $blue;
    }
  }
}
</style>

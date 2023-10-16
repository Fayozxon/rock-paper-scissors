<script>
export default {
  props: ['gameScore'],
  data() {
    return {
        
    }
  }
}
</script>

<template>
    
    <header class="header">
      <div class="container">
        <img src="../assets/logo.svg" alt="Logo" class="header__img">
        <div class="header__score">
          <h2>Score</h2>
          <h1 class="num">{{ gameScore }}</h1>
        </div>
      </div>
    </header>

</template>

<style lang="scss" scoped>
@import '../main.scss';

.header {
    max-width: 700px;
    margin: 0 auto;
    padding: 45px 30px;
    
    .container {
      display: flex;
      align-items: center;
      justify-content: space-between;
      border: 3px solid $color-neutral-200;
      border-radius: 15px;
      padding: 20px 25px;
    }

    &__img {
      width: 30%;
    }

    &__score {
      padding: 15px 40px;
      background: $color-neutral-100;
      color: $color-accent-100;
      border-radius: 10px;
      text-align: center;
      font-size: 1rem;

      .num {
        font-size: 4rem;
        color: $color-neutral-200;
      }
    }
}

</style>

<script>
import RulesModal from './components/RulesModal.vue';
import Header from './components/Header.vue';
import Playground from './components/Playground.vue';

export default {
  components: {RulesModal, Header, Playground},
  data() {
    return {
      gameScore: 0
    }
  }
}
</script>

<template>
  
  <main class="main">
    
    <RulesModal></RulesModal>
    
    <Header :gameScore="gameScore"></Header>

    <Playground></Playground>

  </main>


</template>

<style lang="scss">
@import './main.scss';

/* Fade transitions */
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition: 200ms;
}

</style>

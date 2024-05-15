<template>
  <div id="app">
    <section class="section">
      <div class="container">
        <BulmaMessage
          title="Kõige olulisem"
          type="is-primary"
          @close="showMessage = false"
          v-if="showMessage"
        >
          ASDIOWHQHUIDHUIAHSOUPUHQIHDUIHWIYTQYSGDYUGUYQGUYO
        </BulmaMessage>

        <BulmaMessage
          title="OHTLIK"
          type="is-danger"
          @close="showDangerMessage = false"
          v-if="showDangerMessage"
        >
          __________:_;;;;;:____:;:__:;:_________:;:_
        </BulmaMessage>

        <BulmaMessage
          title="Töötas"
          type="is-success"
          @close="showSuccessMessage = false"
          v-if="showSuccessMessage"
        >
          Muidugi see töötas
        </BulmaMessage>
      </div>
    </section>
  </div>
</template>

<script>
import BulmaMessage from './components/BulmaMessage.vue';

export default {
  name: 'App',
  components: {
    BulmaMessage
  },
  data() {
    return {
      showMessage: true,
      showDangerMessage: true,
      showSuccessMessage: true
    };
  }
};
</script>

<style>
@import 'bulma/css/bulma.css';

/* Add any global styles here if necessary */
</style>

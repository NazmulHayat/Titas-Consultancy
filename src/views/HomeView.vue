<template>
  <IntroPage />
</template>

<script>
import { defineComponent } from 'vue';

// Components
import IntroPage from '../components/IntroPage.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    IntroPage,
  },
});
</script>

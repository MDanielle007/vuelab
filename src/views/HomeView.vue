<template>
  <TeamSection />
</template>

<script>
import { defineComponent } from 'vue';

// Components
import TeamSection from '../components/TeamSection.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    TeamSection,
  },
});
</script>

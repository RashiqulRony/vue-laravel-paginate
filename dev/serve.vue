<script>
import Vue from 'vue';
import VueLaravelPaginate from '@/vue-laravel-paginate.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VueLaravelPaginate
  }
});
</script>

<template>
  <div id="app">
    <vue-laravel-paginate />
  </div>
</template>

<template>
  <div id="app">
    <the-header></the-header>
    <div class="d-flex flex-column w-100">
      <component :is="page" ></component>
    </div>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader'
import User from './components/features/User/UserVue';
import Admin from './components/features/Admin/AdminVue';
import {eventBus} from './main';

export default {
  name: 'app',
  components: {
    TheHeader,
    User,
    Admin
  },
  data() {
    return {
      page: eventBus.page
    }
  },
  created() {
  eventBus.$on('update:page', (page) => {
    this.page = page;
  })
}
}
</script>
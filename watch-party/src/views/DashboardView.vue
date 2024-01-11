<template>
    <div>
      <h1>Welcome, {{ username }}</h1>
      <AdminFeatures v-if="isAdmin" />
      <UserFeatures v-else />
    </div>
</template>
  
<script>
  import { computed } from 'vue';
  import AdminFeatures from '../components/AdminFeatures.vue';
  import UserFeatures from '../components/UserFeatures.vue';
  
  export default {
    components: {
      AdminFeatures,
      UserFeatures
    },
    setup() {
      const username = computed(() => {
        // Get username logic
        return "Sathyam"
      });
      const isAdmin = computed(() => {
        // Admin check logic
        return false;
      });
  
      return {
        username,
        isAdmin
      };
    }
  };
</script>
  
<template>
  <div class="users">
    <users-page/>
  </div>
</template>

<script>
// @ is an alias to /src
import UsersPage from '@/components/UsersPage.vue'

export default {
  name: 'Users',
  components: {
    UsersPage
  }
}
</script>

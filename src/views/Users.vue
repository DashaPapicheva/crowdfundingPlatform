<template>
  <div class="users">
    <UsersPage/>
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

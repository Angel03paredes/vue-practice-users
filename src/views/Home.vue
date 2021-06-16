<template>
  <div >
    <UserList></UserList>
  </div>
</template>

<script>
// @ is an alias to /src
import UserList from '@/components/UserList.vue'
import "../../node_modules/bootswatch/dist/materia/bootstrap.min.css"

export default {
  name: 'Home',
  components: {
    UserList
  }
}
</script>

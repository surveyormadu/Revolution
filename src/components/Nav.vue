<template>
  <nav>
    <div>
      <h1><strong>Team</strong> Revolution</h1>

      <div class="menu">
        <li>
          Surveillance
        </li>
        <li class="active">
          Inbox
        </li>
        <li>
          Data Report
        </li>
        <li>
          Footages
        </li>
        <li>
          Route Analysis
        </li>
      </div>

      <div v-if="isLogin" class="login">
        <Avatar :src="user.photoURL" />
        <button class="text-gray-400 hover:text-white" @click="signOut">
          Sign Out
        </button>
      </div>

      <button v-else class="bg-green-500 hover:bg-green-600" @click="signIn">
        Sign in
      </button>
    </div>
  </nav>
</template>

<script>
import Avatar from './Avatar.vue'
import { useAuth } from '@/firebase'

export default {
  components: { Avatar },
  setup() {
    const { user, isLogin, signOut, signIn } = useAuth()
    return { user, isLogin, signOut, signIn }
  }
}
</script>

<style scoped>
.menu {
  display: flex;
}

li {
  list-style: none;
  color: white;
  margin: 0 10px;
}

.active {
  background: grey;
  border-radius: 8px;
  padding: 2px 8px;
}
</style>

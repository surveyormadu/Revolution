<template>
  <div class="main-control">
    <Nav />
    <!-- <div class="control1"></div> -->

    <div class="chat">
      <chat></chat>
    </div>

    <div class="control2"></div>
  </div>
</template>

<script>
import Nav from '@/components/Nav.vue'
import Chat from '@/components/Chat.vue'

export default {
  name: 'App',
  components: { Nav, Chat }
}
</script>

<style scoped>
h1 {
  color: #ffffff;
  text-align: center;
  margin-top: 5px;
}
.main-control {
  width: 100%;
  display: flex;
}

.menu {
  margin: 0.4rem auto 0.2rem auto;
  width: 80%;
}

.active {
  background: grey;
  border-radius: 8px;
  padding: 12px 8px;
}

.control2 {
  width: 80%;
  height: 100vh;
  background: green;
}

.s-text {
  vertical-align: super;
  margin-left: 5px;
}

.chat {
  height: 100vh;
  overflow-y: auto;
}
</style>

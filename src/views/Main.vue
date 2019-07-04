<template>
  <div class="row flex-grow-1 bg-white mx-0">
    <div class="col-md-4 d-none d-md-block border-right h-100 px-0">
      <UserList />
    </div>
    <div class="col-md-8 h-100 px-0">
      <Chat />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

import UserList from "@/components/UserList.vue";
import Chat from "@/components/Chat.vue";

@Component({
  components: {
    UserList,
    Chat
  }
})
export default class Main extends Vue {}
</script>


<style>
.bg-white {
  background: white;
}
</style>

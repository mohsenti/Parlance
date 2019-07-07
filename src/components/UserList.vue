<template>
  <div>
    <div class="search-panel d-flex flex-column align-items-center p-2">
      <b-input type="text" placeholder="Search" />
    </div>
    <User v-for="user in users" v-bind:key="user.uniqueName" :info="user" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import User from "@/components/User.vue";
import { UserModel } from "@/models";

@Component({
  components: {
    User
  }
})
export default class UserList extends Vue {
  public users: UserModel[] = [];
  mounted() {
    for (let i = 1; i < 10; i++) {
      this.users.push({
        name: i.toString(),
        uniqueName: i.toString(),
        avatarURL: i.toString(),
        lastMessage: i.toString(),
        lastMessageTime: i.toString(),
        budget: i
      });
    }
  }
}
</script>


<style>
.search-panel {
  height: 58px;
  text-align: center;
}
</style>

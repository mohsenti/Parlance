<template>
  <div class="user-panel d-flex flex-column p-2 border-top">
    <div class="row mx-0" style="flex-wrap: nowrap">
      <div class="user-avatar">
        <b-img :src="info.avatarURL" width="48px" height="48px" />
      </div>
      <div class="d-flex mx-0 flex-column" style="max-width: 70%;">
        <div class="user-info mx-2">Mohsen Timar</div>
        <div class="user-info mx-2">akharin chizi ke goftam yadete ?</div>
      </div>
      <div class="d-flex mx-0 flex-column">
        <div class="mx-2" style="width:40px">11:20</div>
        <div class="mx-2" style="width:40px">40</div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from "vue-property-decorator";
import { UserModel } from "../models";
@Component
export default class User extends Vue {
  @Prop({ default: undefined })
  public info?: UserModel;
}
</script>


<style>
.user-panel {
  height: 65px;
}
.user-avatar {
}
.user-info {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>

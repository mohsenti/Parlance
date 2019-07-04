<template>
  <div>
    <div class="search-panel d-flex flex-column align-items-center p-2 border-bottom">
      <b-input type="text" placeholder="Search" />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component
export default class UserList extends Vue {}
</script>


<style>
.search-panel {
  height: 58px;
  text-align: center;
}
</style>

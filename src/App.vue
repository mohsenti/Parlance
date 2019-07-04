<template>
  <div id="app" class="h-100">
    <div class="container-fluid container-margin d-flex flex-column h-100">
      <div class="head row">
        <div class="col-md-4 d-none h-100 d-md-table px-0">
          <div class="d-table-cell align-middle">
            <div class="col-sm-12 px-4 d-flex align-items-center">
              <span class="mi mi-menu pr-4"></span>
              Parlance
            </div>
          </div>
        </div>
        <div class="col-md-8 col-sm-12 h-100 d-table px-0">
          <div class="d-table-cell align-middle">
            <div class="px-4">Connecting ...</div>
          </div>
        </div>
      </div>
      <div class="row flex-grow-1">
        <Main />
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Main from "./views/Main.vue";
@Component({
  components: {
    Main
  }
})
export default class App extends Vue {
  mounted() {}
}
</script>

<style lang="scss">
#app {
  text-align: center;
  background-color: rgb(231, 235, 240);
}
.head {
  height: 48px;
  background: rgb(86, 130, 163);
}
.container-margin {
  max-width: 1000px;
  margin: 0px auto;
  text-align: left;
}
</style>

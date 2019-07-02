<template>
  <div class="home"></div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import SocketIO from "socket.io-client";
@Component
export default class Home extends Vue {
  private io: SocketIOClient.Socket;
  constructor() {
    super();
    this.io = SocketIO("http://localhost:3001");
    this.io.on("connect", (socket: any) => {
      console.log("Connected");
      this.io.emit("message", "HelloWorld");
    });
    this.io.on("message", (msg: any) => {
      console.log(msg);
    });
    this.io.on("disconnect", () => {
      console.log("DisConnected");
    });
  }
}
</script>

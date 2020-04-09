<template>
  <footer class="footer">
    <div class="container-fluid">
      <ul class="nav">
        <li class="nav-item">
          <a href="#" class="copyright" v-on:click="show()">Add Line For Ad</a>
        </li>
      </ul>
      <div class="copyright">
        &copy;
        {{ new Date().getFullYear() }} made with
        <i class="tim-icons icon-heart-2"></i> by
        <a href="https://github.com/UPThawatchai" target="_blank">SUPERUP</a>.
      </div>
    </div>
    <div id="modal">
      <modal name="qrcode">
        <vue-qr
          :bgSrc="src"
          :logoSrc="src2"
          :size="256"
          text="http://line.me/ti/p/~sinjugu"
          colorDark="#3a683f"
          style="width: fit-content;height: fit-content;"
        ></vue-qr>
      </modal>
    </div>
  </footer>
</template>
<script>
import Vue from "vue";
import VModal from "vue-js-modal";
import VueQr from "vue-qr";
Vue.component("vue-qr", VueQr);
Vue.use(VModal);
export default {
  //value: "http://line.me/ti/p/~sinjugu",
  methods: {
    show: function() {
      this.$modal.show("qrcode");
    },
    hide() {
      this.$modal.hide("qrcode");
    }
  }
};
</script>
<style>
</style>





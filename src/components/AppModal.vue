<template>
    <div v-if="visible">
        <div class="app-modal" @click.prevent="visible = false"></div>
        <div class="app-modal-inner">
            <a href="#" @click.prevent="visible = false">Close</a>
            <slot name="body" :params="params" />
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      params: {},
      visible: false
    };
  },
  props: {
    name: {
      required: true,
      type: String
    }
  },
  mounted() {
    this.$modal.$event.$on("show", (modal, params) => {
      if (this.name === modal) {
        this.params = params;
        this.visible = true;
      }
    });
  }
};
</script>


<style>
.app-modal {
  background-color: #141420;
  position: fixed;
  width: 100%;
  height: 100%;
  z-index: 9999;
  top: 0;
  left: 0;
}

.app-modal-inner {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: #fff;
  padding: 30px;
  width: 90%;
  max-width: 500px;
  border-radius: 3px;
  z-index: 9999;
}
</style>

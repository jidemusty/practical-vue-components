<template>
    <transition name="modal">
      <div v-if="visible">
        <div class="app-modal" @click.prevent="$modal.hide(name)"></div>
        <div class="app-modal-inner">
            <a href="#" @click.prevent="$modal.hide(name)">Close</a>
            <slot name="body" :params="params" />
        </div>
    </div>
    </transition>
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
  methods: {
    setVisible() {
      this.visible = true;
    },
    setHidden() {
      this.visible = false;
    }
  },
  beforeMount() {
    this.$modal.$event.$on("show", (modal, params) => {
      if (this.name !== modal) {
        return;
      }

      this.params = params;

      if (!this.$listeners["before-open"]) {
        this.setVisible();
        return;
      }

      this.$emit("before-open", () => {
        this.setVisible();
      });
    });

    this.$modal.$event.$on("hide", modal => {
      if (this.name === modal) {
        this.setHidden();
      }
    });
  },
  mounted() {
    document.addEventListener("keydown", e => {
      if (this.visible && e.keyCode === 27) {
        this.visible = false;
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

.modal-enter-active,
.modal-leave-active {
  transition: all 200ms;
}

.modal-enter,
.modal-leave-active {
  opacity: 0;
}
</style>

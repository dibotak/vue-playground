<template>
  <div v-if="modal2" class="nav-modal-container">
    <transition name="modal-left" appear @enter="$emit('toggle-status')" @before-enter="$emit('d-status', true)">
      <div v-if="leftBg" :class="['nav-modal-left']"></div>
    </transition>
    <transition name="modal-right" appear @after-leave="closePlease" @after-enter="activate">
      <div v-if="rightBg" :class="['nav-modal-right']"></div>
    </transition>
    <div class="nav-modal-content">
      <transition name="left-nav" @after-leave="setBg(false)" @after-enter="$emit('d-status', false)" @before-leave="$emit('d-status', true)">
        <div v-if="cLeft" class="content-left">
        </div>
      </transition>
      <div class="content-main">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['show'],
  data() {
    return {
      modal2: false,
      transition: false,
      leftBg: true,
      rightBg: true,
      cLeft: false,
      text: [false,false,false,false,false],
    }
  },
  computed: {
    modal() {
      return this.show
    }
  },
  methods: {
    setBg(val) {
      this.leftBg = val
      this.rightBg = val
    },
    closePlease() {
      this.modal2 = false
      this.$emit('d-status', false)
      this.setBg(true)
    },
    activate() {
      this.cLeft = true
    },
    closeModal() {
      this.$emit('toggle-status')
      this.cLeft = false
    }
  },
  watch: {
    modal(val) {
      if (val) {
        this.modal2 = true
      } else {
        this.closeModal()
      }
    }
  }
}
</script>

<style scoped>
.nav-modal-container {
  display: flex;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  /* background-color: blanchedalmond; */
}

.nav-modal-left {
  background-color: aliceblue;
  width: 30%;
  transform: translateY(0);
}

.nav-modal-right {
  background-color: aliceblue;
  width: 70%;
  transform: translateY(0);
}

.nav-modal-active {
  transform: translateY(0);
}

.nav-modal-content {
  position: absolute;
  display: flex;
  top: 0;
  z-index: 5;
  width: 100%;
}

.nav-modal-header {
  position: absolute;
  top: 0;
  display: flex;
  justify-content: end;
  width: 100%;
}

.to-center {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100vh;
}

.content-left {
  width: 30%;
  background-color: white;
  height: 100vh;
}

/* BACKGROUND TRANSITION */
.modal-left-enter {
  transform: translateY(-100%);
}

.modal-left-leave-to {
  transform: translateY(150%);
}

.modal-left-enter-active {
  transition: transform .3s;
}

.modal-left-leave-active {
  transition: transform .5s;
}

.modal-right-enter {
  transform: translateY(-100%);
}

.modal-right-leave-to {
  transform: translateY(100%);
}

.modal-right-enter-active, .modal-right-leave-active {
  transition: transform .3s;
  transition-delay: 0.2s;
}
/* --- BACKGROUND TRANSITION END --- */

/* BODY MODAL NAV TRANSITION */
.left-nav-enter-active, .left-nav-leave-active {
  transition: transform .3s;
}

.left-nav-enter, .left-nav-leave-to {
  transform: translateX(-100%);
}

/* --- BODY MODAL NAV END --- */

</style>

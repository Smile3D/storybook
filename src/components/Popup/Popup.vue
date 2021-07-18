<template>
    <div v-show="is_opened">
        <div class="popup-overlay" @click="close"></div>
        <div class="popup">
            <button @click="close" class="close-popup"></button>
            <div class="popup-container">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      is_opened: false
    }
  },
  methods: {
    open () {
      this.$emit('openPopup', this.is_opened = true)
    },
    close () {
      this.is_opened = false
      console.log('sdasd')
    }
  }
}
</script>

<style lang="scss" scoped>
.popup-overlay {
  background-color: rgba(#000, 0.5);
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
  z-index: 99;
}
.popup {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    position: fixed;
    z-index: 999;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: #fff;
    border-radius: 14px;
    padding: 20px 30px;
    max-width: 1160px;
    width: calc(100% - 20px);
}

.close-popup {
  display: block;
  width: 20px;
  height: 20px;
  position: absolute;
  top: 22px;
  right: 10px;
  cursor: pointer;
  padding: 0;

  &:hover {
    &:after,
    &:before {
      background-color: #1b48c0;
    }
  }

  &:after,
  &:before {
    content: "";
    position: absolute;
    background-color: #dadceb;
    width: 2px;
    height: 20px;
    top: 0;
  }

  &:after {
    transform: rotate(45deg);
  }

  &:before {
    transform: rotate(-45deg);
  }
}
</style>

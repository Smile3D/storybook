<template>
<div>
  <button
    :disabled="disabled"
    :class="`btn ${additionalClass} ${textColor} ${btnSize}`"
  >
    {{ textBtn }}
  </button>
  <div class="description-block">
    <h3>Описание компонента</h3>
  </div>
</div>
</template>

<script>
export default {
  name: 'Btn',
  props: {
    additionalClass: String,
    textBtn: String,
    textColor: String,
    disabled: Boolean,
    btnSize: String
  }
}
</script>

<style scoped lang="scss">

.btn {
  transition: background-color 0.3s;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: center;
  border: none;
  min-width: 200px;
  min-height: 40px;
  border-radius: 40px;
  padding: 10px 20px;
  font-size: 14px;
  letter-spacing: 1px;
  text-transform: uppercase;
  font-weight: 600;
  background-color: transparent;
  cursor: pointer;

  &:disabled {
    background-color: #FFCB8D;

    &:hover {
      background-color: #FFCB8D;
    }
  }

  &--rounded {
    border-radius: 50%;
  }

  &--bg-primary {
    background-color: blue;

    &:hover {
      background-color: orange;
    }
  }

  &--bg-secondary {
    background-color: #ff9d2b;

    &:hover {
      background-color: #ff951a;
    }
  }

  &--color-text-primary {
    color: #fff;
  }

  &--color-text-secondary {
    color: blue;
  }

  &--outline {
    border: 1px solid blue;

    &:hover {
      background-color: blue;
      color: #fff;
    }
  }
}

.description-block {
  border-radius: 10px;
  background-color: #011627;
}
</style>

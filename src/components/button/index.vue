<template>
  <button
    class="wqh-button"
    :class="[theme, isRound, isBorder, isSize]"
    :disabled="disabled"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'index',
  props: {
    type: {
      type: String,
      default: ''
    },
    size: {
      type: String,
      default: ''
    },
    round: Boolean,
    border: Boolean,
    disabled: Boolean
  },
  computed: {
    theme() {
      return this.type ? `wqh-button-${this.type}` : ''
    },
    isRound() {
      return this.round ? 'is-round' : ''
    },
    isBorder() {
      return this.border ? 'is-border' : ''
    },
    isSize() {
      return this.size ? `wqh-button-${this.size}` : ''
    }
  }
}
</script>

<style lang="scss" scoped>
.wqh-button {
  border-width: 1px;
  border-style: solid;
  border-color: #dcdfe6;
  height: 40px;
  padding: 0 20px;
  background-color: #fff;
  border-radius: 4px;
  font-size: 14px;
  color: #606266;
  cursor: pointer;

  + .wqh-button {
    margin-left: 14px;
  }
}
.wqh-button-medium {
  height: 38px;
}
.wqh-button-small {
  padding: 0 15px;
  height: 32px;
  font-size: 12px;
}
.wqh-button-mini {
  padding: 0 15px;
  height: 28px;
  font-size: 12px;
}
.wqh-button[disabled] {
  cursor: not-allowed;
  opacity: 0.5;
}
.wqh-button-primary {
  background-color: #409eff;
  border-color: #409eff;
  color: #fff;
  &.is-border {
    background-color: transparent;
    color: #409eff;
  }
}
.wqh-button-success {
  background-color: #00d100;
  border-color: #00d100;
  color: #fff;
  &.is-border {
    background-color: transparent;
    color: #00d100;
  }
}
.wqh-button-danger {
  background-color: #e6a23c;
  border-color: #e6a23c;
  color: #fff;
  &.is-border {
    background-color: transparent;
    color: #e6a23c;
  }
}
.wqh-button-warning {
  background-color: #f56c6c;
  border-color: #f56c6c;
  color: #fff;
  &.is-border {
    background-color: transparent;
    color: #f56c6c;
  }
}

/**
 * 圆角
 */
.is-round {
  border-radius: 100px;
}
</style>

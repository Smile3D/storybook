<template>
    <select
      :name="name"
      :id="id"
      value="value"
    >
    <slot></slot>
    </select>
</template>

<script>
export default {
  props: ['name', 'id', 'value']
}
</script>

<style lang="scss" scoped>

</style>

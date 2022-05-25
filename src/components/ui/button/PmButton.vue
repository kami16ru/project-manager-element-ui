<template>
  <el-button
    v-bind="$attrs"
    v-on="$listeners"
  >
    <slot v-for="(_, name) in $slots" :slot="name" :name="name" />
    <template v-for="(_, name) in $scopedSlots" :slot="name" slot-scope="slotData">
      <slot :name="name" v-bind="slotData" />
    </template>
  </el-button>
</template>

<script>
export default {
  props: {

  }
}
</script>

<style scoped>

</style>

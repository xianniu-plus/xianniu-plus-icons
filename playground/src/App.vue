<script lang="ts" setup>
import { icons } from '@xianniu-plus/icons-vue/global'
import { Upload } from '@xianniu-plus/icons-vue'
</script>

<template>
  <Upload class="icon" />
  <hr />
  <component :is="Icon" v-for="(Icon, key) in icons" :key="key" class="icon" />
  <hr />
  <component
    :is="`ElIcon${key}`"
    v-for="key in Object.keys(icons)"
    :key="key"
    class="icon"
  />
</template>

<style>
.icon {
  height: 48px;
  color: #409eff;
}
</style>

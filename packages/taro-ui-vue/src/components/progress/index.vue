<template>
  <view :class="rootClass(status)">
    <view class="at-progress__outer">
      <view class="at-progress__outer-inner">
        <view
          class="at-progress__outer-inner-background"
          :style="progressStyle"
        />
      </view>
    </view>
    <view v-if="!isHidePercent" class="at-progress__content">
      <view v-if="!status || status === 'progress'">
        {{ `${percent}%` }}
      </view>
      <view v-else>
        <view :class="iconClass()" />
      </view>
    </view>
  </view>
</template>

<script lang="ts">
import AtProgress from './index'
export default AtProgress
</script>

<template>
  <div class="timeline-container">
    <el-timeline style="max-width: 1000px">
      <el-timeline-item v-for="(activity, index) in activities" :key="index" :timestamp="activity.timestamp">
        <el-link :href="activity.link" target="_blank" class="large-font-timeline">{{ activity.content
          }}</el-link>
      </el-timeline-item>
    </el-timeline>
  </div>
</template>

<script lang="ts" setup>
const activities = [
  {
    content: '以太坊 GAS 预测工具',
    link: 'https://gas.33357.xyz',
    timestamp: '2023-10-13',
  },
  {
    content: 'XEN 批量挖矿工具',
    link: 'https://xenbox.33357.xyz',
    timestamp: '2023-5-25',
  },
  // {
  //   content: '以太坊地址聊天',
  //   link: 'https://chat.33357.xyz',
  //   timestamp: '2024-3-13',
  // },
  // {
  //   content: '在线计算 create2',
  //   link: 'https://create2.33357.xyz',
  //   timestamp: '2024-3-13',
  // },
]
</script>

<style>
.timeline-container {
  position: absolute;
  top: 10%;
  left: 40%;
  transform: translateX(-50%);
}

.large-font-timeline {
  font-size: 2em;
}
</style>
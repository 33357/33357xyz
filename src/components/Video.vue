<template>
  <div class="timeline-container">
    <el-timeline style="max-width: 1000px">
      <el-timeline-item
        v-for="(activity, index) in activities"
        :key="index"
        :timestamp="activity.timestamp"
      >
        <el-link
          :href="activity.link"
          target="_blank"
          class="large-font-timeline"
          >{{ activity.content }}</el-link
        >
      </el-timeline-item>
    </el-timeline>
  </div>
</template>

<script lang="ts" setup>
const activities = [
  {
    content: "Flashbot 隐私节点的运用",
    link: "https://b23.tv/R7IkqYX",
    timestamp: "2024-3-5",
  },
  {
    content: "铭文带来的新机会",
    link: "https://b23.tv/U2CgccB",
    timestamp: "2024-2-4",
  },
  {
    content: "最小代理合约的原理和运用",
    link: "https://b23.tv/UleFdu6",
    timestamp: "2023-10-30",
  },
  {
    content: "智能合约工程师的赚钱方法",
    link: "https://b23.tv/6INoM7j",
    timestamp: "2023-10-16",
  },
  {
    content: "合约重入攻击",
    link: "https://b23.tv/0MZsiZj",
    timestamp: "2022-8-2",
  },
];
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

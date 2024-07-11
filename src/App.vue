<template>
  <el-config-provider namespace="ep">
    <el-menu
      :default-active="activeIndex"
      mode="horizontal"
      :ellipsis="false"
      @select="handleSelect"
    >
      <el-menu-item index="1" class="item"> 文章 </el-menu-item>
      <el-menu-item index="2" class="item"> 视频 </el-menu-item>
      <el-menu-item index="3" class="item"> 工具 </el-menu-item>
      <el-menu-item index="-1" class="item" @click="toggleDark()">
        <button
          class="border-none w-full bg-transparent cursor-pointer"
          style="height: var(--ep-menu-item-height)"
        >
          <i inline-flex i="dark:ep-moon ep-sunny" />
        </button>
      </el-menu-item>
      <div class="flex-grow" />
      <el-menu-item index="-2" class="item" @click="toWX()">
        {{ `关注 公众号` }}
      </el-menu-item>
      <el-menu-item index="-3" class="item" @click="toX()">
        {{ `关注 X` }}
      </el-menu-item>
      <el-menu-item index="-4" class="item" @click="toTG()">
        {{ `加入 TG 群` }}
      </el-menu-item>
      <el-menu-item index="-5" class="item" @click="toGithub()">
        {{ `关注 Github` }}
      </el-menu-item>
    </el-menu>
    <div>
      <Article v-if="activeIndex == '1'"></Article>
      <Video v-if="activeIndex == '2'"></Video>
      <Tool v-if="activeIndex == '3'"></Tool>
    </div>
  </el-config-provider>
</template>

<script lang="ts">
import { useDark, useToggle } from "@vueuse/core";
import { utils, log } from "./const";
import { mapState, mapActions } from "vuex";
import { State } from "./store";

export default {
  data() {
    return {
      utils,
      activeIndex: "1",
      toggleDark: useToggle(useDark()),
    };
  },
  created() {
    window.addEventListener("load", async () => {
      // const chainId = Number(utils.func.getParameterByName("c"));
      // const gasLimitInput = utils.func.getParameterByName("g");
      // log(`window load ${chainId} ${gasLimitInput}`);
      // await this.start({ chainId });
      // if (
      //   gasLimitInput &&
      //   Number(gasLimitInput) > 0 &&
      //   Number(gasLimitInput) <= 30000000
      // ) {
      //   this.state.storage.gasLimitInput = gasLimitInput;
      // }
    });
  },
  computed: mapState({
    state: (state: any) => state as State,
  }),
  methods: {
    ...mapActions(["start"]),
    toWX() {
      window.open("/wx.jpg", "_blank");
    },
    toX() {
      window.open("https://x.com/33357xyz", "_blank");
    },
    toTG() {
      window.open("https://t.me/smartcontractapps", "_blank");
    },
    toGithub() {
      window.open("https://github.com/33357", "_blank");
    },
    handleSelect(key: string) {
      if (Number(key) > 0) {
        (this as any).activeIndex = key;
      }
    },
  },
};
</script>

<style>
#app {
  /* text-align: center; */
  /* color: var(--ep-text-color-primary); */
}

.item {
  width: 7%;
}

.item2 {
  width: 15%;
}

.flex-grow {
  flex-grow: 1;
}
</style>

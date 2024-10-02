<template>
  <v-card class="mx-auto rounded-0" width="100%" height="100%">
    <!-- 暗黑主题选项卡 -->
    <v-tabs
      v-if="theme.global.current.value.dark"
      show-arrows
      align-tabs="center"
      center-active
      v-model="tab"
      style="background-color: #0c0c0c; opacity: 0.8"
      next-icon="mdi-step-forward"
      prev-icon="mdi-step-backward"
      color="indigo-accent-1"
    >
      <v-tab value="one">欧穆首页</v-tab>
      <v-tab value="two">服务流程</v-tab>
      <v-tab value="three">设备定价</v-tab>
      <v-tab value="six">关于我们</v-tab>
    </v-tabs>

    <!-- light主题选项卡开始 -->
    <v-tabs
      v-else
      show-arrows
      align-tabs="center"
      center-active
      v-model="tab"
      style="background: linear-gradient(#bbe2ff, 40%, #e8f4fd); opacity: 1"
      class="text-medium-emphasis"
      next-icon="mdi-step-forward"
      prev-icon="mdi-step-backward"
      color="indigo-accent-1"
    >
      <v-tab value="one">欧穆首页</v-tab>
      <v-tab value="two">服务流程</v-tab>
      <v-tab value="three">设备定价</v-tab>
      <v-tab value="six">关于我们</v-tab>
    </v-tabs>

    <v-window v-model="tab">
      <!-- 首页 -->
      <v-window-item value="one">
        <home></home>
      </v-window-item>
      <!-- 服务流程 -->
      <v-window-item value="two">
        <process></process>
      </v-window-item>
      <!-- 设备价格 -->
      <v-window-item value="three">
        <price></price>
      </v-window-item>
      <!-- 企业原则 -->
      <v-window-item value="six">
        <culture></culture>
      </v-window-item>
    </v-window>
  </v-card>
</template>

<script setup>
import home from "../pages/home";
import process from "../pages/process";
import price from "../pages/price";
import culture from "../pages/culture";
import { ref } from "vue";
import { useTheme } from "vuetify";
const theme = useTheme();

const range = ref([100, 1000000]);
const firstName = ref("");

const rules = [
  (value) => {
    if (value) return true;
    return "填下呗，仅用于称呼您";
  },
];

const model = ref("接受");
</script>

<script>
export default {
  data: () => ({
    tab: null,
    fwdialog: false,
    tjdialog: false,
    notifications: false,
    sound: true,
    widgets: false,
    model: true,
  }),
};
</script>

<style>
.v-slide-group__next,
.v-slide-group__prev {
  color: #0091ff;
}

/* 脚注字体大小 */
@media screen and (max-width: 400px) {
  .fonsi {
    font-size: 10px;
  }

  .v-card {
    font-size: 12px;
  }
}

@media screen and (min-width: 401px) {
  .fonsi {
    font-size: 13px;
  }
  .v-card {
    font-size: 14px;
  }
}

@media screen and (min-width: 500px) {
  .v-card {
    font-size: 15px;
  }
}

.v-table {
  font-size: 13px;
  line-height: 20px;
}
</style>

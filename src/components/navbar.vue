<template>
  <!-- 海洋主题顶部导航栏开始 -->
  <v-app-bar
    style="background-color: #161616; opacity: 0.7"
    v-if="theme.global.current.value.dark"
    :elevation="3"
    scroll-behavior="fade-image elevate"
    scroll-threshold="1000"
    fade-image
    round
    inverted
  >
    <template v-slot:prepend>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
    </template>
    <v-app-bar-title text-subtitle-1>欧穆云软件</v-app-bar-title>
    <template v-slot:append>
      <!-- 搜索框 -->
      <v-btn prepend-icon="mdi-magnify" color="indigo-accent-1">
        <v-dialog
          style="opacity: 0.9"
          v-model="dialog"
          activator="parent"
          width="89%"
          max-width="700"
        >
          <v-card class="pa-3 rounded-xl">
            <v-text-field
              class="py-4 pb-5 text-indigo-accent-1"
              v-model="search"
              clearable
              hide-details
              label="用Bing搜一下吧"
              prepend-inner-icon="mdi-magnify"
              single-line
              @keyup.enter="performSearch"
            ></v-text-field>
            <v-card-actions>
              <v-btn color="indigo-accent-1" @click="dialog = false">close</v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-btn>
      <!-- 搜索框结束 -->
      <!-- 主题切换按钮 -->
      <v-btn
        v-if="theme.global.current.value.dark"
        @click="toggleTheme"
        color="indigo-accent-1"
        icon="mdi-weather-sunny"
      ></v-btn>
      <v-btn v-else @click="toggleTheme" icon="mdi-weather-night"></v-btn>
    </template>
  </v-app-bar>
  <!-- 顶部导航结束 -->
  <!-- 海洋主题顶部导航栏结束 -->

  <!-- light主题顶部导航开始 -->
  <v-app-bar
    v-else
    style="opacity: 0.68"
    :elevation="3"
    scroll-behavior="fade-image elevate"
    scroll-threshold="1000"
    class="text-blue"
    fade-image
    round
    inverted
  >
    <template v-slot:prepend>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
    </template>
    <v-app-bar-title text-subtitle-1>欧穆云软件</v-app-bar-title>
    <template v-slot:append>
      <!-- 搜索框 -->
      <v-btn prepend-icon="mdi-magnify">
        <v-dialog v-model="dialog" activator="parent" width="89%" max-width="700">
          <v-card class="pa-3 rounded-xl">
            <v-text-field
              class="py-4 pb-5 text-blue"
              v-model="search"
              clearable
              hide-details
              label="用Bing搜一下吧"
              prepend-inner-icon="mdi-magnify"
              single-line
              @keyup.enter="performSearch"
            ></v-text-field>
            <v-card-actions>
              <v-btn color="blue" @click="dialog = false">close</v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-btn>
      <!-- 搜索框结束 -->

      <!-- 主题切换按钮 -->
      <v-btn
        v-if="theme.global.current.value.dark"
        @click="toggleTheme"
        icon="mdi-weather-sunny"
      ></v-btn>
      <v-btn v-else @click="toggleTheme" icon="mdi-weather-night"></v-btn>
    </template>
  </v-app-bar>
  <!-- light顶部导航结束 -->

  <!-- 海洋主题抽屉导航开始 -->
  <v-navigation-drawer
    style="background-color: #111111; opacity: 0.9"
    v-if="theme.global.current.value.dark"
    app
    v-model="drawer"
  >
    <v-list>
      <v-list-item
        style="color: rgb(0 192 255)"
        prepend-avatar="../assets/tx.jpg"
        title="葛墨林"
        subtitle="QQ:1778607946"
      >
        <template v-slot:append>
          <v-btn
            color="yellow"
            size="small"
            variant="text"
            icon="mdi-creation"
            href="https://tzgml.pages.dev/"
          ></v-btn>
        </template>
      </v-list-item>
    </v-list>
    <v-divider :thickness="2" class="border-opacity-50" color="white"></v-divider>
    <v-list
      class="text-medium-emphasis text-white font-weight-bold px-4 pt-5 pb-16 mx-auto"
    >
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :value="item"
        color="primary"
        rounded="xl"
        :href="item.to"
      >
        <template v-slot:prepend>
          <v-icon color="indigo-accent-1" :icon="item.icon"></v-icon>
        </template>
        <v-list-item-title v-text="item.text"></v-list-item-title>
      </v-list-item>
    </v-list>
    <template v-slot:append>
      <div class="mx-4 mb-15 w-70">
        <v-btn
          block
          class="text-indigo-accent-1 font-weight-bold"
          elevation="2"
          prepend-icon="mdi-github"
          variant="tonal"
          href="https://github.com/TZGML"
          >Github</v-btn
        >
      </div>
    </template>
  </v-navigation-drawer>

  <!-- 海洋主题抽屉导航结束 -->

  <!-- light主题抽屉导航开始 -->
  <v-navigation-drawer style="opacity: 0.86" v-else app v-model="drawer">
    <v-list>
      <v-list-item
        prepend-avatar="../assets/tx.jpg"
        title="葛墨林"
        subtitle="QQ:1778607946"
      >
        <template v-slot:append>
          <v-btn
            size="small"
            variant="text"
            icon="mdi-creation"
            color="yellow-accent-4"
            href="https://tzgml.pages.dev/"
          ></v-btn>
        </template>
      </v-list-item>
    </v-list>
    <v-divider :thickness="2" class="border-opacity-50" color="blue"></v-divider>
    <v-list class="text-blue-accent-3 font-weight-bold px-4 pt-5 pb-16 mx-auto">
      <v-list-item
        v-for="(item, i) in items"
        :key="i"
        :value="item"
        color="primary"
        rounded="xl"
        :href="item.to"
      >
        <template v-slot:prepend>
          <v-icon :icon="item.icon"></v-icon>
        </template>
        <v-list-item-title v-text="item.text"></v-list-item-title>
      </v-list-item>
    </v-list>
    <template v-slot:append>
      <div class="mx-4 mb-15 w-70">
        <v-btn
          block
          class="text-indigo-accent-1 font-weight-bold"
          elevation="2"
          prepend-icon="mdi-github"
          variant="tonal"
          href="https://github.com/TZGML"
          >Github</v-btn
        >
      </div>
    </template>
  </v-navigation-drawer>
  <!-- light抽屉导航结束 -->
</template>

<script setup>
import { ref } from "vue";
import { useTheme } from "vuetify";
const items = [
  {
    text: "本站Vuetify版",
    icon: "$vuetify",
    to: "https://ougml.pages.dev",
  },
  {
    text: "GMLstartpage",
    icon: "mdi-play-box-multiple",
    to: "https://tzgemolin.pages.dev",
  },
  {
    text: "Rumi官方Doc",
    icon: "mdi-language-markdown",
    to: "https://milang.programapps.top/docs/rumi",
  },
  {
    text: "GPT- nextweb",
    icon: "mdi-robot-excited",
    to: "https://ai.programapps.top",
  },
  {
    text: "欧穆FastCDN",
    icon: "mdi-cloud-search",
    to: "https://fast.programapps.top",
  },
  {
    text: "ICMT 管理器",
    icon: "mdi-git",
    to: "https://pan.programapps.top/ICMT",
  },
  {
    text: "PS CLangIDE",
    icon: "mdi-language-cpp",
    to: "https://github.com/program-zoubg/CLangIDE",
  },
  {
    text: "LayUI版 官网",
    icon: "mdi-alpha-l-circle",
    to: "https://tzgml.pages.dev",
  },
  {
    text: "VantUI版官网",
    icon: "mdi-alpha-v-box",
    to: "https://oumuvant.pages.dev",
  },
  {
    text: "ElementUI 式",
    icon: "mdi-alpha-e-box",
    to: "https://oumueui.pages.dev",
  },
];
// 抽屉式导航
const drawer = ref(null);
//更改颜色主题
const theme = useTheme();
function toggleTheme() {
  theme.global.name.value = theme.global.current.value.dark ? "light" : "dark";
}
// 弹出搜索对话框
const dialog = ref(false);
</script>

<script>
export default {
  data() {
    return {
      drawer: null,
      search: "",
    };
  },
  methods: {
    // 搜索框
    performSearch() {
      window.location.href = "https://www.bing.com/search?q=" + this.search;
    },
  },
};
</script>

<template>
  <!-- 暗黑主题轮播图开始 -->
  <v-carousel
    v-if="theme.global.current.value.dark"
    interval="2500"
    cycle
    hide-delimiter-background
    show-arrows="hover"
    progress="indigo-accent-1"
  >
    <v-carousel-item color="black" cover>
      <div class="d-flex fill-height justify-center align-center">
        <div
          class="text-h4 text-md-h2 text-lg-h1 text-xl-h1 text-xxl-h1 font-weight-bold text-indigo-accent-1"
        >
          诚信
        </div>
      </div>
    </v-carousel-item>
    <v-carousel-item color="black" cover>
      <div class="d-flex fill-height justify-center align-center">
        <div
          class="text-h4 text-md-h2 text-lg-h1 text-xl-h1 text-xxl-h1 font-weight-bold text-indigo-accent-1"
        >
          高效
        </div>
      </div>
    </v-carousel-item>
    <v-carousel-item color="black" cover>
      <div class="d-flex fill-height justify-center align-center">
        <div
          class="text-h4 text-md-h2 text-lg-h1 text-xl-h1 text-xxl-h1 font-weight-bold text-indigo-accent-1"
        >
          专业
        </div>
      </div>
    </v-carousel-item>
    <v-carousel-item color="black" cover>
      <div class="d-flex fill-height justify-center align-center">
        <div
          class="text-h4 text-md-h2 text-lg-h1 text-xl-h1 text-xxl-h1 font-weight-bold text-indigo-accent-1"
        >
          专一
        </div>
      </div>
    </v-carousel-item>
  </v-carousel>
  <!-- 暗黑主题轮播图结束 -->

  <!-- 明亮主题轮播图开始 -->
  <v-carousel
    v-else
    interval="2500"
    cycle
    hide-delimiter-background
    show-arrows="hover"
    progress="indigo-accent-1"
  >
    <v-carousel-item color="grey-lighten-4" cover>
      <div class="d-flex fill-height justify-center align-center">
        <div
          class="text-h4 text-md-h2 text-lg-h1 text-xl-h1 text-xxl-h1 font-weight-bold text-indigo-accent-1"
        >
          诚信
        </div>
      </div>
    </v-carousel-item>
    <v-carousel-item color="grey-lighten-4" cover>
      <div class="d-flex fill-height justify-center align-center">
        <div
          class="text-h4 text-md-h2 text-lg-h1 text-xl-h1 text-xxl-h1 font-weight-bold text-indigo-accent-1"
        >
          高效
        </div>
      </div>
    </v-carousel-item>
    <v-carousel-item color="grey-lighten-4" cover>
      <div class="d-flex fill-height justify-center align-center">
        <div
          class="text-h4 text-md-h2 text-lg-h1 text-xl-h1 text-xxl-h1 font-weight-bold text-indigo-accent-1"
        >
          专业
        </div>
      </div>
    </v-carousel-item>
    <v-carousel-item color="grey-lighten-4" cover>
      <div class="d-flex fill-height justify-center align-center">
        <div
          class="text-h4 text-md-h2 text-lg-h1 text-xl-h1 text-xxl-h1 font-weight-bold text-indigo-accent-1"
        >
          专一
        </div>
      </div>
    </v-carousel-item>
  </v-carousel>
  <!-- 明亮主题轮播图结束 -->

  <!-- 暗黑主题时间线开始 -->
  <v-card
    v-if="theme.global.current.value.dark"
    class="mx-auto pa-3 pb-10 pt-6 rounded-0 text-indigo-accent-1"
    width="100%"
    prepend-icon="mdi-book-clock-outline"
    append-icon="mdi-clock-time-seven"
    title="欧穆时间线"
    subtitle="回顾以往"
  >
    <v-card ma-4>
      <v-timeline
        class="mx-2"
        density="compact"
        line-color="indigo-accent-1"
        line-thickness="4"
        side="end"
      >
        <v-timeline-item dot-color="light-blue-accent-3" size="small">
          <v-alert
            border="start"
            title="2023.2.1"
            value="true"
            class="bg-black text-indigo-accent-1"
            icon="mdi-account-hard-hat-outline"
            >欧穆云非营利组织构想初具雏形，按照最初的设想进行长达一年的小规模实践，团队3次迭代，商业计划书重构18次，至今已基本稳定，平稳发展。我们将提供开源强大的产品以及解决方案。
            欧穆云坚定不移的支持自由软件的发展，并尽自己最大的努力推动软件行业的发展进步。我们认为软件科技更多的应当为工农大众服务，而不是反过来用于监控，压迫人民群众，恩格斯指出“科学越是毫无顾忌和大公无私，它越符合工人的利益和愿望。”因此欧穆云（不包括自团队）所有产品都将成为自由软件。
            欧穆云将始终为工农服务，并计划于2025年开放各种便利工人维权/学习/交流的小程序与APP，欧穆云的软件外包业务仅仅只是为了本非营利组织能够继续存续，而为工人服务是欧穆云真正的初心与使命。我们不会相其他的非营利组织一样开放捐款渠道，欧穆云不需要，我们自己可以维持自己的生存并尽自己最大的努力方便广大的工人同志们。
          </v-alert>
        </v-timeline-item>
        <v-timeline-item fill-dot dot-color="yellow" size="small">
          <v-alert
            border="start"
            title="2024.1.18"
            value="true"
            class="bg-black text-indigo-accent-1"
            icon="mdi-alpha-r-circle-outline"
          >
            由欧穆云非营利子团队programspace用rust开发的全新的，完整的，跨平台的编程语言Rumi,其原型为C++开发的Milang，其RumiIDE编译器GUI界面用pyQt开发。Rumi借鉴了其他语言的优良特性，
            它的语法和特性与python非常相似，但Rumi的语法更加简洁，更加符合现代编程语言的特性。目前正在飞速发展，扩充大量语法，Rumi将成为一个极其强大完整，简单易学的现代化编程语言，Rumi的原则是“精简、安全、快速”，我们的代码经过反复的调试，优化，审计，确保编译内核精简快速。
            Rumi的编译器GUI界面，将支持代码补全，语法高亮，代码格式化，代码自动补全，代码自动。Rumi正在持续开发中，敬请期待。
          </v-alert>
        </v-timeline-item>
        <v-timeline-item dot-color="deep-purple-accent-1" size="small">
          <v-alert
            title="2024.2.18"
            border="end"
            value="true"
            class="bg-black text-indigo-accent-1"
            icon="mdi-source-repository-multiple"
          >
            由于github有单个文件25MB的上传限制，并且一次不能上传太多文件，导致大项目很难存储，虽然可以用github
            LFS，但是这个工具上手有门槛，对纯小白不太友好，因此欧穆云子团队programspace开发出Program
            Repos，用户可以使用极其简单的upload和clone命令轻松上传大文件，理论上支持最大一次性上传100MB的项目，没有上传文件数量和单个文件大小的限制，
            使用`ls
            用户名`即可查看自己的仓库，用clone即可下载，服务器在国内，因此速度会快很多。Program
            Repos也有Linux版本Repo
            Bash，但目前只支持命令行，后续将会开发出pyQTGUI界面，此项目正在持续扩充更多的功能，以期提供更多更优质的服务。
          </v-alert>
        </v-timeline-item>
        <v-timeline-item dot-color="pink-accent-1" size="small">
          <v-alert
            title="2024.2.23"
            border="end"
            value="true"
            class="bg-black text-indigo-accent-1"
            icon="mdi-warehouse"
            >由欧穆云子团队programspace开发的一个极其简洁、美观的原生C/C++集成开发环境（IDE），抛去一切o多余繁琐的配置，专注于代码编写，目前仅支持Windows7以上的系统，CLangIDE是建立在构建一个纯原生集成开发环境IDE的基础上的。PyQtMinGW/GCC由于
            GCC编译器后缀的限制，编辑器会识别用于保存源代码和确定源代码类型的文件配置;对于C，保留默认值（写“c”），对于
            C++，写“cpp”。支持通过python部署，源码已发布到github：
            https://github.com/program-zoubg/CLangIDE，正在持续开发中。
          </v-alert>
        </v-timeline-item>
      </v-timeline>
    </v-card>
  </v-card>
  <!-- 暗黑主题时间线结束 -->

  <!-- light主题时间线开始 -->
  <v-card
    v-else
    class="mx-auto pa-3 pb-10 pt-6 rounded-0 text-indigo-accent-1"
    width="100%"
    prepend-icon="mdi-book-clock-outline"
    append-icon="mdi-clock-time-seven"
    title="欧穆时间线"
    subtitle="回顾以往"
  >
    <v-card ma-4>
      <v-timeline
        class="mx-2"
        density="compact"
        line-color="indigo-accent-1"
        line-thickness="4"
        side="end"
      >
        <v-timeline-item dot-color="light-blue-accent-3" size="small">
          <v-alert
            border="start"
            title="2023.2.1"
            value="true"
            color="indigo-accent-1"
            icon="mdi-account-hard-hat-outline"
            >欧穆云非营利组织构想初具雏形，按照最初的设想进行长达一年的小规模实践，团队3次迭代，商业计划书重构18次，至今已基本稳定，平稳发展。我们将提供开源强大的产品以及解决方案。
            欧穆云坚定不移的支持自由软件的发展，并尽自己最大的努力推动软件行业的发展进步。我们认为软件科技更多的应当为工农大众服务，而不是反过来用于监控，压迫人民群众，恩格斯指出“科学越是毫无顾忌和大公无私，它越符合工人的利益和愿望。”因此欧穆云（不包括自团队）所有产品都将成为自由软件。
            欧穆云将始终为工农服务，并计划于2025年开放各种便利工人维权/学习/交流的小程序与APP，欧穆云的软件外包业务仅仅只是为了本非营利组织能够继续存续，而为工人服务是欧穆云真正的初心与使命。我们不会相其他的非营利组织一样开放捐款渠道，欧穆云不需要，我们自己可以维持自己的生存并尽自己最大的努力方便广大的工人同志们。
          </v-alert>
        </v-timeline-item>
        <v-timeline-item fill-dot dot-color="yellow" size="small">
          <v-alert
            border="start"
            title="2024.1.18"
            value="true"
            color="indigo-accent-1"
            icon="mdi-alpha-r-circle-outline"
          >
            由欧穆云非营利子团队programspace用rust开发的全新的，完整的，跨平台的编程语言Rumi,其原型为C++开发的Milang，其RumiIDE编译器GUI界面用pyQt开发。Rumi借鉴了其他语言的优良特性，
            它的语法和特性与python非常相似，但Rumi的语法更加简洁，更加符合现代编程语言的特性。目前正在飞速发展，扩充大量语法，Rumi将成为一个极其强大完整，简单易学的现代化编程语言，Rumi的原则是“精简、安全、快速”，我们的代码经过反复的调试，优化，审计，确保编译内核精简快速。
            Rumi的编译器GUI界面，将支持代码补全，语法高亮，代码格式化，代码自动补全，代码自动。Rumi正在持续开发中，敬请期待。
          </v-alert>
        </v-timeline-item>
        <v-timeline-item dot-color="deep-purple-accent-1" size="small">
          <v-alert
            title="2024.2.18"
            border="end"
            value="true"
            color="indigo-accent-1"
            icon="mdi-source-repository-multiple"
          >
            由于github有单个文件25MB的上传限制，并且一次不能上传太多文件，导致大项目很难存储，虽然可以用github
            LFS，但是这个工具上手有门槛，对纯小白不太友好，因此欧穆云子团队programspace开发出Program
            Repos，用户可以使用极其简单的upload和clone命令轻松上传大文件，理论上支持最大一次性上传100MB的项目，没有上传文件数量和单个文件大小的限制，
            使用`ls
            用户名`即可查看自己的仓库，用clone即可下载，服务器在国内，因此速度会快很多。Program
            Repos也有Linux版本Repo
            Bash，但目前只支持命令行，后续将会开发出pyQTGUI界面，此项目正在持续扩充更多的功能，以期提供更多更优质的服务。
          </v-alert>
        </v-timeline-item>
        <v-timeline-item dot-color="pink-accent-1" size="small">
          <v-alert
            title="2024.2.19"
            border="end"
            value="true"
            color="indigo-accent-1"
            icon="mdi-warehouse"
          >
            受到Arch
            linux的用户仓库AUR的启发，以及国内互联网的切实需要，欧穆云计划推出OMUR软件仓库，主要提供受到封锁的国际软件以及代理软件，用户可以上传自己的软件包，也可以下载他人提供的软件包，支持exe,apk,deb,pkg.tar.zst等等包，
            欧穆云坚决遵守我国法律法规，对于黄赌毒以及暴力软件坚决封禁，确保omur均为国际上正规的软件，和普通的软件商店一样的下载/安装/更新方式。一般用途就是为了在装系统之后，可以尽快解决网络问题。用户在使用新设备时，登陆omur账户即可查看在其他设备安装的应用程序列表，并可以一键全部安装在新设备上，更换设备时极为方便。
          </v-alert>
        </v-timeline-item>
      </v-timeline>
    </v-card>
  </v-card>
  <!-- light主题时间线结束 -->

  <v-card
    class="mx-auto pa-3 pt-10 rounded-0 text-indigo-accent-1"
    width="100%"
    prepend-icon="mdi-lightbulb-on-90"
    append-icon="mdi-lightbulb-on-90"
  >
    <v-card variant="plain" elevation="4" class="mt-6 mx-4">
      <v-footer class="text-medium-emphasis my-5 text-center d-flex flex-column">
        <p style="line-height: 27px">
          2025 |徐州欧穆云软件科技合伙企业(普通合伙)©版权所有
        </p>
        <img width="150px" src="../assets/wx.png" alt="欧穆云软件科技" />
        <p style="line-height: 27px">添加微信：gemolin66</p>
        <p style="line-height: 27px">企业临时负责人：葛墨林</p>

        <p style="line-height: 27px">电话：021-18952131771|传真:021-72342355</p>

        <p style="line-height: 27px">苏公网安备31890805607697号 | 苏ICP备1504646号-1</p>
        <p style="line-height: 27px">总部：徐州市鼓楼区金山桥三环东路E20创意园A栋六楼</p>
        <p>服务政策 | 加入我们 | 联系我们</p>
      </v-footer>
    </v-card>
  </v-card>
</template>

<script setup>
import { ref } from "vue";
import { useTheme } from "vuetify";
const theme = useTheme();
</script>

<style lang="scss" scoped>
.v-footer p {
  font-size: 12px;
}
@media screen and (max-width: 400px) {
  .v-footer p {
    font-size: 9px;
    line-height: normal;
  }
  .v-footer img {
    width: 70px;
  }
}
</style>

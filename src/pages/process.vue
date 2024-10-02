<template>
  <!-- 海洋主题步骤条开始 -->
  <v-stepper
    v-if="theme.global.current.value.dark"
    mobile
    class="rounded-0"
    prev-text="前一步"
    next-text="后一步"
    color="white"
    alt-labels
    :items="[
      '需求对接',
      '价格协商',
      '周期确认',
      '定金协商',
      '签订合同',
      '立项开发',
      '交付客户',
      '售后服务',
    ]"
  >
    <template v-slot:item.1>
      <v-card class="text-light-blue-accent-1" title="需求对接" flat
        >客户描述需求 ➣ 我方确认需求 ➣ 双方确定需求
        <v-list lines="two">
          <v-list-item
            title="描述需求"
            subtitle="将需求与预期效果详细描述，如果有清晰易懂的需求文档和原型图更好，便于我们理解并为您提供服务"
            :prepend-icon="'mdi-comment-quote'"
          ></v-list-item>
          <v-list-item
            title="确认需求"
            subtitle="我方整理出需求文档与原型图，交予您审阅是否符合其需求，不符的地方进行更改，确保您的需求与我方理解一致"
            :prepend-icon="'mdi-account-check'"
          ></v-list-item>
          <v-list-item
            title="确定需求"
            subtitle="请您确定需求，确保后期不大幅度更改或提出全新需求，否则我们会面临返工复工，甚至代码重构的麻烦，严重拖延项目周期"
            :prepend-icon="'mdi-file-chart-check'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>

    <template v-slot:item.2>
      <v-card title="价格协商" class="text-light-blue-accent-1" flat
        >提出报价 🢣 询问预算 🢣 价格调整 🢣 确立定价
        <v-list lines="two">
          <v-list-item
            subtitle="我们将结合需求与人力成本对项目进行报价，如有需要，将整理出详细的价目表"
            title="提出报价"
            :prepend-icon="'mdi-account-cash-outline'"
          ></v-list-item>
          <v-list-item
            title="询问预算"
            subtitle="我们报价后，会询问您的预算，确保符合您的心理预期"
            :prepend-icon="'mdi-frequently-asked-questions'"
          ></v-list-item>
          <v-list-item
            title="价格调整"
            subtitle="根据我方报价与您的预算，您可以和我们充分协商，我们将尽可能将定价贴近您的预算"
            :prepend-icon="'mdi-format-align-middle'"
          ></v-list-item>
          <v-list-item
            title="确立定价"
            subtitle="在我们充分的协商交流之后，最终确立项目价格"
            :prepend-icon="'mdi-bank-check'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>

    <template v-slot:item.3>
      <v-card title="开发周期" class="text-light-blue-accent-1" flat
        >我方评估开发周期 ⇛ 客户提出需要期限 ⇛ 我方调整时间安排 ⇛ 最终确立开发周期

        <v-list lines="two">
          <v-list-item
            title="评估周期"
            subtitle="我们根据项目需求、项目难度、项目人员安排等因素，评估项目周期"
            :prepend-icon="'mdi-clipboard-clock'"
          ></v-list-item>
          <v-list-item
            title="客户预期"
            subtitle="您根据自身实际情况提出时间要求，我们根据实际情况调整时间安排"
            :prepend-icon="'mdi-message-text-clock'"
          ></v-list-item>
          <v-list-item
            title="时间调整"
            subtitle="根据您的需要，我们会对我们的安排进行调整，确保符合您的预期"
            :prepend-icon="'mdi-timer-edit'"
          ></v-list-item>
          <v-list-item
            title="确立周期"
            subtitle="在我们充分的协商交流之后，最终确立项目开发周期"
            :prepend-icon="'mdi-timeline-check-outline'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.4>
      <v-card title="定金协商" class="text-light-blue-accent-1" flat
        >定金协商 » 确定定金

        <v-list lines="two">
          <v-list-item
            title="定金协商"
            subtitle="根据您的实际情况，可以选择2+6+2，3+4+3，5+5等其他自定义付款模式，优先支持3+4+3"
            :prepend-icon="'mdi-currency-jpy'"
          ></v-list-item>
          <v-list-item
            title="确定定金"
            subtitle="3+4+3即开发前交付30%定金，大体框架完成后交付40%，项目完成后交付30%尾款，其他模式以此类推"
            :prepend-icon="'mdi-hand-coin-outline'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.5>
      <v-card title="签订合同" class="text-light-blue-accent-1" flat
        >总结需求，周期，定金，价格等协商结果 ➾ 草拟合同 ➾ 合同签订

        <v-list lines="two">
          <v-list-item
            title="磋商总结"
            subtitle="总结各个要素的磋商结果"
            :prepend-icon="'mdi-collapse-all-outline'"
          ></v-list-item>
          <v-list-item
            title="草拟合同"
            subtitle="我方草拟合同，交予您确认（您们可以要求自己起草）"
            :prepend-icon="'mdi-pencil-box-multiple'"
          ></v-list-item>
          <v-list-item
            title="签订合同"
            subtitle="合同经各方确认，签字，盖章，生效，开始项目开发"
            :prepend-icon="'mdi-map-check'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.6>
      <v-card title="立项开发" class="text-light-blue-accent-1" flat
        >项目开发 + 进度反馈 + 效果确认

        <v-list lines="two">
          <v-list-item
            title="项目开发"
            subtitle="我们一定马不停蹄，保质保量，按时按质完成项目"
            :prepend-icon="'mdi-cloud-braces'"
          ></v-list-item>
          <v-list-item
            title="进度反馈"
            subtitle="每当项目完成到一定节点，便会向您汇报进度，您也可随时要求询问开发进度"
            :prepend-icon="'mdi-timeline-question'"
          ></v-list-item>
          <v-list-item
            title="效果确认"
            subtitle="当我们完成一部分功能或界面，将其展示给您确认是否符合达到预期效果"
            :prepend-icon="'mdi-eye-check'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.7>
      <v-card title="项目交付" class="text-light-blue-accent-1" flat
        >开发完成 ⇢ 交付项目 ⇢ 客户验收

        <v-list lines="two">
          <v-list-item
            title="开发完成"
            subtitle="在您确认了需求实现后，我们将把项目交付给您"
            :prepend-icon="'mdi-television-stop'"
          ></v-list-item>
          <v-list-item
            title="交付项目"
            subtitle="该项目整个源码全部打包交付您，可自行部署，也可要求我们进行部署"
            :prepend-icon="'mdi-account-arrow-left'"
          ></v-list-item>
          <v-list-item
            title="客户验收"
            subtitle="请您确认验收后交付尾款，之后双方发信息进行确认"
            :prepend-icon="'mdi-message-check-outline'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.8>
      <v-card title="售后服务" class="text-light-blue-accent-1" flat
        >上线部署 + bug修复 + 二次开发（ 迭代更新 | 性能优化 | 样式美化 | 功能更改 ）
        <v-list lines="two">
          <v-list-item
            title="上线部署全免费"
            subtitle="对于网站，您可以自选服务器，对于App,小程序，您可指定上线平台"
            :prepend-icon="'mdi-kubernetes'"
          ></v-list-item>
          <v-list-item
            title="bug修复全免费"
            subtitle="产品出现bug即时联系我们，我们一定尽最快速度解决"
            :prepend-icon="'mdi-cog-sync'"
          ></v-list-item>
          <v-list-item
            title="二次开发"
            subtitle="根据工程量确定收费，但确保低价收费"
            :prepend-icon="'mdi-office-building-plus'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
  </v-stepper>
  <!-- 海洋主题步骤条结束 -->

  <!-- light theme主题步骤条 -->
  <!-- light theme主题步骤条 -->
  <v-stepper
    v-else
    mobile
    class="text-blue-lighten-1"
    prev-text="前一步"
    next-text="后一步"
    color="blue"
    alt-labels
    :items="[
      '需求对接',
      '价格协商',
      '周期确认',
      '定金协商',
      '签订合同',
      '立项开发',
      '交付客户',
      '售后服务',
    ]"
  >
    <template v-slot:item.1>
      <v-card class="text-light-blue-accent-3" title="需求对接" flat
        >客户描述需求 ➣ 我方确认需求 ➣ 双方确定需求
        <v-list class="text-blue" lines="two">
          <v-list-item
            title="描述需求"
            subtitle="将需求与预期效果详细描述，如果有清晰易懂的需求文档和原型图更好，便于我们理解并为您提供服务"
            :prepend-icon="'mdi-comment-quote'"
          ></v-list-item>
          <v-list-item
            title="确认需求"
            subtitle="我方整理出需求文档与原型图，交予您审阅是否符合其需求，不符的地方进行更改，确保您的需求与我方理解一致"
            :prepend-icon="'mdi-account-check'"
          ></v-list-item>
          <v-list-item
            title="确定需求"
            subtitle="请您确定需求，确保后期不大幅度更改或提出全新需求，否则我们会面临返工复工，甚至代码重构的麻烦，严重拖延项目周期"
            :prepend-icon="'mdi-file-chart-check'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>

    <template v-slot:item.2>
      <v-card class="text-deep-purple-lighten-1" title="价格协商" flat
        >提出报价 🢣 询问预算 🢣 价格调整 🢣 确立定价
        <v-list class="text-deep-purple-accent-2" lines="two">
          <v-list-item
            title="提出报价"
            subtitle="我们将结合需求与人力成本对项目进行报价，如有需要，将整理出详细的价目表"
            :prepend-icon="'mdi-account-cash-outline'"
          ></v-list-item>
          <v-list-item
            title="询问预算"
            subtitle="我们报价后，会询问您的预算，确保符合您的心理预期"
            :prepend-icon="'mdi-frequently-asked-questions'"
          ></v-list-item>
          <v-list-item
            title="价格调整"
            subtitle="根据我方报价与您的预算，您可以和我们充分协商，我们将尽可能将定价贴近您的预算"
            :prepend-icon="'mdi-format-align-middle'"
          ></v-list-item>
          <v-list-item
            title="确立定价"
            subtitle="在我们充分的协商交流之后，最终确立项目价格"
            :prepend-icon="'mdi-bank-check'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>

    <template v-slot:item.3>
      <v-card class="text-light-blue-accent-3" title="开发周期" flat
        >我方评估开发周期 ⇛ 客户提出需要期限 ⇛ 我方调整时间安排 ⇛ 最终确立开发周期

        <v-list class="text-light-blue-darken-1" lines="two">
          <v-list-item
            title="评估周期"
            subtitle="我们根据项目需求、项目难度、项目人员安排等因素，评估项目周期"
            :prepend-icon="'mdi-clipboard-clock'"
          ></v-list-item>
          <v-list-item
            title="客户预期"
            subtitle="您根据自身实际情况提出时间要求，我们根据实际情况调整时间安排"
            :prepend-icon="'mdi-message-text-clock'"
          ></v-list-item>
          <v-list-item
            title="时间调整"
            subtitle="根据您的需要，我们会对我们的安排进行调整，确保符合您的预期"
            :prepend-icon="'mdi-timer-edit'"
          ></v-list-item>
          <v-list-item
            title="确立周期"
            subtitle="在我们充分的协商交流之后，最终确立项目开发周期"
            :prepend-icon="'mdi-timeline-check-outline'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.4>
      <v-card class="text-indigo-lighten-1" title="定金协商" flat
        >定金协商 » 确定定金

        <v-list class="text-deep-purple-lighten-1" lines="two">
          <v-list-item
            title="定金协商"
            subtitle="根据您的实际情况，可以选择2+6+2，3+4+3，5+5等其他自定义付款模式，优先支持3+4+3"
            :prepend-icon="'mdi-currency-jpy'"
          ></v-list-item>
          <v-list-item
            title="确定定金"
            subtitle="3+4+3即开发前交付30%定金，大体框架完成后交付40%，项目完成后交付30%尾款，其他模式以此类推"
            :prepend-icon="'mdi-hand-coin-outline'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.5>
      <v-card class="text-indigo-accent-1" title="签订合同" flat
        >总结需求，周期，定金，价格等协商结果 ➾ 草拟合同 ➾ 合同签订

        <v-list class="text-indigo-accent-2" lines="two">
          <v-list-item
            title="磋商总结"
            subtitle="总结各个要素的磋商结果"
            :prepend-icon="'mdi-collapse-all-outline'"
          ></v-list-item>
          <v-list-item
            title="草拟合同"
            subtitle="我方草拟合同，交予您确认（您们可以要求自己起草）"
            :prepend-icon="'mdi-pencil-box-multiple'"
          ></v-list-item>
          <v-list-item
            title="签订合同"
            subtitle="合同经各方确认，签字，盖章，生效，开始项目开发"
            :prepend-icon="'mdi-map-check'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.6>
      <v-card class="text-light-blue-darken-1" title="立项开发" flat
        >项目开发 + 进度反馈 + 效果确认

        <v-list class="text-light-blue-lighten-1" lines="two">
          <v-list-item
            title="项目开发"
            subtitle="我们一定马不停蹄，保质保量，按时按质完成项目"
            :prepend-icon="'mdi-cloud-braces'"
          ></v-list-item>
          <v-list-item
            title="进度反馈"
            subtitle="每当项目完成到一定节点，便会向您汇报进度，您也可随时要求询问开发进度"
            :prepend-icon="'mdi-timeline-question'"
          ></v-list-item>
          <v-list-item
            title="效果确认"
            subtitle="当我们完成一部分功能或界面，将其展示给您确认是否符合达到预期效果"
            :prepend-icon="'mdi-eye-check'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.7>
      <v-card class="text-light-blue-darken-2" title="项目交付" flat
        >开发完成 ⇢ 交付项目 ⇢ 客户验收

        <v-list class="text-light-blue-darken-4" lines="two">
          <v-list-item
            title="开发完成"
            subtitle="在您确认了需求实现后，我们将把项目交付给您"
            :prepend-icon="'mdi-television-stop'"
          ></v-list-item>
          <v-list-item
            title="交付项目"
            subtitle="该项目整个源码全部打包交付您，可自行部署，也可要求我们进行部署"
            :prepend-icon="'mdi-account-arrow-left'"
          ></v-list-item>
          <v-list-item
            title="客户验收"
            subtitle="请您确认验收后交付尾款，之后双方发信息进行确认"
            :prepend-icon="'mdi-message-check-outline'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
    <template v-slot:item.8>
      <v-card class="text-cyan-accent-3" title="售后服务" flat
        >上线部署 + bug修复 + 二次开发（ 迭代更新 | 性能优化 | 样式美化 | 功能更改 ）
        <v-list class="text-cyan-accent-4" lines="two">
          <v-list-item
            title="上线部署全免费"
            subtitle="对于网站，您可以自选服务器，对于App,小程序，您可指定上线平台"
            :prepend-icon="'mdi-kubernetes'"
          ></v-list-item>
          <v-list-item
            title="bug修复全免费"
            subtitle="产品出现bug即时联系我们，我们一定尽最快速度解决"
            :prepend-icon="'mdi-cog-sync'"
          ></v-list-item>
          <v-list-item
            title="二次开发"
            subtitle="根据工程量确定收费，但确保低价收费"
            :prepend-icon="'mdi-office-building-plus'"
          ></v-list-item>
        </v-list>
      </v-card>
    </template>
  </v-stepper>

  <!-- 海洋主题服务列表开始 -->
  <v-card
    v-if="theme.global.current.value.dark"
    class="mx-auto pa-3 pb-10 pt-6 rounded-0 text-indigo-accent-1"
    style="height: 100%"
    width="100%"
    prepend-icon="mdi-clipboard-list-outline"
    append-icon="mdi-nuxt"
    title="服务列表"
    subtitle="我们要为您提供哪些服务呢"
  >
    <v-expansion-panels class="mt-3" multiple="true" variant="accordion">
      <v-expansion-panel
        class="text-medium-emphasis"
        rounded="xl"
        title="安卓与IOS移动应用APP原生开发"
        text="使用Flutter开发跨平台移动应用，效果极其贴近原生，高质量开发，快速交付"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-medium-emphasis"
        rounded="lg"
        title="多端小程序与微信公众号开发与上线"
        text="用uniapp等技术开发多端小程序，包含微信，QQ，支付宝，抖音，百度等各大平台"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-medium-emphasis"
        rounded="lg"
        title="优质网站设计,开发与部署,外包与定制服务"
        text="使用vue3+springboot+MySQL等技术组合开发响应式自适应网站，完美适配各种设备"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-medium-emphasis"
        rounded="lg"
        title="跨平台（win,linux,macOS）桌面应用开发"
        text="Qt或electron开发跨平台桌面应用，涵盖Windows,Linux,MacOS"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-medium-emphasis"
        rounded="lg"
        title="智能硬件嵌入式系统专业外包服务"
        text="Linux+stm32+C+Qt开发嵌入式系统与现代上位机程序"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-medium-emphasis"
        rounded="lg"
        title="针对网站，各类应用的现代化精美UI设计"
        text="使用先进UI设计工具，打造精妙绝伦的现代化用户界面"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-medium-emphasis"
        rounded="xl"
        title="网站托管，云存储等各种优质云服务"
        text="配置优，性能好，价格低，速度快，轻管控，售后服务到位的欧穆云"
      >
      </v-expansion-panel>
    </v-expansion-panels>
  </v-card>
  <!-- 海洋主题服务列表结束 -->

  <!-- light主题服务列表 -->
  <v-card
    v-else
    class="bg-white text-indigo mx-auto pa-4 rounded-lg mt-10 pb-10"
    style="height: 100%"
    width="100%"
    prepend-icon="mdi-clipboard-list-outline"
    append-icon="mdi-nuxt"
    title="服务列表"
    subtitle="我们要为您提供哪些服务呢"
  >
    <v-expansion-panels class="mt-3" multiple="true" variant="accordion">
      <v-expansion-panel
        class="text-blue-lighten-1"
        rounded="lg"
        title="安卓与IOS移动应用APP原生开发"
        text="使用Flutter开发跨平台移动应用，效果极其贴近原生，高质量开发，快速交付"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-blue-lighten-1"
        rounded="lg"
        title="多端小程序与微信公众号开发与上线"
        text="用uniapp等技术开发多端小程序，包含微信，QQ，支付宝，抖音，百度等各大平台"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-blue-lighten-1"
        rounded="lg"
        title="优质网站设计,开发与部署,外包与定制服务"
        text="使用vue3+springboot+MySQL等技术组合开发响应式自适应网站，完美适配各种设备"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-blue-lighten-1"
        rounded="lg"
        title="跨平台（win,linux,macOS）桌面应用开发"
        text="Qt或electron开发跨平台桌面应用，涵盖Windows,Linux,MacOS"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-blue-lighten-1"
        rounded="lg"
        title="智能硬件嵌入式系统专业外包服务"
        text="Linux+stm32+C+Qt开发嵌入式系统与现代上位机程序"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-blue-lighten-1"
        rounded="lg"
        title="针对网站，各类应用的现代化精美UI设计"
        text="使用先进UI设计工具，打造精妙绝伦的现代化用户界面"
      >
      </v-expansion-panel>
      <v-expansion-panel
        class="text-blue-lighten-1"
        rounded="lg"
        title="网站托管，云存储等各种优质云服务"
        text="配置优，性能好，价格低，速度快，轻管控，售后服务到位的欧穆云"
      >
      </v-expansion-panel>
    </v-expansion-panels>
  </v-card>
</template>

<script setup>
import { ref } from "vue";
import { useTheme } from "vuetify";
const theme = useTheme();
</script>

<style lang="scss" scoped></style>

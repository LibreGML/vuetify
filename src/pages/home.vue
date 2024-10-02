<template>
  <!-- 首页海洋主题的“认识欧穆云” -->
  <v-card
    v-if="theme.global.current.value.dark"
    style="background-color: #111111; opacity: 0.7"
    class="mx-auto px-2 pt-4 pb-8 rounded-0 text-indigo-accent-1"
    prepend-icon="mdi-vuetify"
    append-icon="mdi-electron-framework"
    title="认识OuMuCloud"
    subtitle="以强大的业务能力服务客户"
  >
    <v-card
      style="background-color: #111111; opacity: 0.89"
      class="mx-auto my-3 px-4 py-3 rounded-lg"
      variant="tonal"
      width="100%"
      prepend-icon="mdi-microsoft-teams"
      append-icon="mdi-compass-rose"
      title="关于团队"
      subtitle="实现客户的需求是我们矢志不渝的使命"
      hover
      >徐州欧穆云软件科技合伙企业（普通合伙）提供全面的质优价廉的专业软件外包服务
      <br />
      企业技术栈丰富，适用于各种业务（H5网站，移动APP,小程序，微信公众号，桌面应用，爬虫等等）,我们有充分的实力与信心实现客户需求。<br />
      企业所有技术人员均为全栈工程师，技术水平成熟，拥有丰富的项目开发，维护，团队协作的相关经验，使用github
      teams,replit teams相互配合，共同高质量的完成项目并快速交付。<br />
      我们贯彻坚守"客户至上"的原则，以客户利益为根本出发点和落脚点，全心全意为客户服务，始终把客户利益放在第一位，尽全力确保快速无误地交付令客户满意的高质量项目。<br />
    </v-card>

    <v-card
      style="background-color: #111111; opacity: 0.89"
      variant="tonal"
      class="mx-auto my-3 px-4 py-3 rounded-lg"
      width="100%"
      prepend-icon="mdi-microsoft-dynamics-365"
      append-icon="mdi-lightning-bolt-outline"
      title="丰富的技术栈"
      subtitle="客户自由选择项目技术栈"
      hover
      >客户可在我们能力范围内自由选择技术栈进行项目开发<br />
      对于APP,可选Flutter/uniapp跨平台开发安卓/IOS两端，或kotlin与swift分别原生开发<br />
      对于桌面应用，可用electron/Qt快速开发跨平台（Windows,MacOS,linux）桌面应用<br />
      对于小程序，我们通常用uniapp多端平台快速部署小程序。<br />
      对于网站，我们支持客户自由选择前后端技术栈，数据库与UI框架<br />
      目前前后端框架支持vue3+springboot/thinkPHP/Flask。数据库支持MySQL
      <br />
      CSS框架优先支持vuetify,其次是LayUI,vant,ElementUI,Tailwind
      <br />
    </v-card>

    <v-card
      style="background-color: #111111; opacity: 0.89"
      variant="tonal"
      class="mx-auto my-3 px-4 py-3 mb-5 rounded-lg"
      width="100%"
      prepend-icon="mdi-cube-scan"
      append-icon="mdi-klingon"
      title="扩展业务"
      subtitle="更多的扩展业务等您探索"
      hover
      >web:爬取海量资源/数据（合法范围内） <br />
      UI设计:助力构建精美现代化UI界面/logo/图标等 <br />
      云服务:高配低价的网站托管/云存储服务 <br />
    </v-card>

    <!-- 对话框面板 -->
    <v-card-actions>
      <v-btn
        variant="tonal"
        rounded="lg"
        elevation="4"
        append-icon="mdi-chevron-double-up"
        >服务列表
        <v-dialog
          v-model="fwdialog"
          :scrim="false"
          transition="dialog-bottom-transition"
          activator="parent"
          fullscreen
        >
          <v-card
            style="background-color: #111111; opacity: 0.955; height: 100%"
            class="mx-auto pa-2 rounded-lg"
            width="100%"
            prepend-icon="mdi-storefront-plus-outline"
            append-icon="mdi-cart-plus"
            title="服务列表"
            subtitle="我们要为您提供哪些服务呢"
          >
            <v-expansion-panels class="mt-3" multiple="true" variant="accordion">
              <v-expansion-panel
                class="text-indigo-accent-1"
                rounded="xl"
                title="安卓与IOS移动应用APP原生开发"
                text="使用Flutter开发跨平台移动应用，效果极其贴近原生，高质量开发，快速交付"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-indigo-accent-1"
                rounded="lg"
                title="多端小程序与微信公众号开发与上线"
                text="用uniapp等技术开发多端小程序，包含微信，QQ，支付宝，抖音，百度等各大平台"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-indigo-accent-1"
                rounded="lg"
                title="优质网站设计,开发与部署,外包与定制服务"
                text="使用vue3+springboot+MySQL等技术组合开发响应式自适应网站，完美适配各种设备"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-indigo-accent-1"
                rounded="lg"
                title="跨平台（win,linux,macOS）桌面应用开发"
                text="Qt或electron开发跨平台桌面应用，涵盖Windows,Linux,MacOS"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-indigo-accent-1"
                rounded="lg"
                title="智能硬件嵌入式系统专业外包服务"
                text="Linux+stm32+C+Qt开发嵌入式系统与现代上位机程序"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-indigo-accent-1"
                rounded="lg"
                title="针对网站，各类应用的现代化精美UI设计"
                text="使用先进UI设计工具，打造精妙绝伦的现代化用户界面"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-indigo-accent-1"
                rounded="xl"
                title="网站托管，云存储等各种优质云服务"
                text="配置优，性能好，价格低，速度快，轻管控，售后服务到位的欧穆云"
              >
              </v-expansion-panel>
            </v-expansion-panels>
            <v-card-actions>
              <v-btn
                class="font-weight-bold mt-4"
                rounded="lg"
                elevation="1"
                append-icon="mdi-chevron-down"
                color="white"
                variant="tonal"
                @click="fwdialog = false"
                >关闭</v-btn
              >
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-btn>
      <v-btn
        variant="tonal"
        rounded="lg"
        elevation="4"
        append-icon="mdi-chevron-double-up"
        >提交需求
        <v-dialog
          v-model="tjdialog"
          fullscreen
          :scrim="false"
          transition="dialog-bottom-transition"
          activator="parent"
          width="100%"
        >
          <v-card
            style="background-color: #111111; opacity: 0.91"
            class="mx-auto px-3 pt-2 rounded-lg"
            width="100%"
            prepend-icon="mdi-puzzle-heart-outline"
            append-icon="mdi-notebook-heart"
            title="提交需求"
            subtitle="我们一定全力以赴完成"
          >
            <v-card class="bg-black px-4 pt-3 mt-3">
              <v-form @submit.prevent>
                <v-text-field
                  class="text-indigo-accent-1"
                  prepend-inner-icon="mdi-card-account-details-star-outline"
                  append-inner-icon="mdi-tag-multiple-outline"
                  clearable
                  label="怎么称呼?"
                  hint="虚拟姓氏也可以，仅为方便称呼您"
                  density="compact"
                >
                </v-text-field>

                <v-text-field
                  class="text-indigo-accent-1"
                  prepend-inner-icon="mdi-phone-message-outline"
                  counter="13"
                  append-inner-icon="mdi-cellphone-message"
                  label="邮箱/手机号/QQ/微信/telegram/signal 等等"
                  hint="优先支持手机/QQ"
                  placeholder="1778607946@qq.com"
                  type="email"
                  clearable
                  density="compact"
                ></v-text-field>
                <v-textarea
                  prepend-inner-icon="mdi-account-circle"
                  append-inner-icon="mdi-email-heart-outline"
                  label="需求描述"
                  placeholder="描述一下您的具体需求，或在下方上传需求文档"
                  hint="尽量上传需求文档或详细描述需求"
                  clearable
                  class="text-blue"
                  density="compact"
                ></v-textarea>
                <v-file-input
                  clearable
                  label="上传需求文档"
                  hint="建议尽量上传"
                  variant="outlined"
                  class="text-indigo-accent-1"
                  density="compact"
                ></v-file-input>

                <v-range-slider
                  label="预算:"
                  thumb-label="always"
                  v-model="range"
                  tick-size="3"
                  track-color="blue-lighten-3"
                  track-fill-color="indigo-accent-1"
                  show-ticks="always"
                  strict
                  :min="100"
                  :max="1000000"
                  hint="可手动输入"
                  density="compact"
                >
                  <template v-slot:prepend>
                    <v-text-field
                      style="width: 91px"
                      class="text-indigo-accent-1"
                      v-model="range[0]"
                      hide-details
                      single-line
                      type="number"
                      variant="outlined"
                      density="compact"
                    ></v-text-field>
                  </template>

                  <template v-slot:append>
                    <v-text-field
                      style="width: 91px"
                      color="blue"
                      class="text-indigo-accent-1"
                      v-model="range[1]"
                      hide-details
                      single-line
                      type="number"
                      variant="outlined"
                      density="compact"
                    ></v-text-field>
                  </template>
                </v-range-slider>

                <v-select
                  class="text-indigo-accent-1"
                  clearable
                  chips
                  lable="项目类型"
                  item-color="blue"
                  :items="[
                    'APP',
                    '小程序',
                    '网站',
                    '桌面应用',
                    '嵌入式',
                    '爬虫',
                    'UI设计',
                    '其他',
                  ]"
                  multiple
                  variant="outlined"
                  hint="可多选"
                  placeholder="APP/小程序/网站/桌面应用"
                  density="compact"
                ></v-select>
                <v-switch
                  color="indigo-accent-1"
                  class="text-blue"
                  v-model="model"
                  hide-details
                  inset
                  density="compact"
                  true-value="接受"
                  false-value="不接受"
                  :label="`是否接受定金: ${model.toString()}`"
                ></v-switch>
                <v-btn class="ml-2 mt-2 text-indigo-accent-1" type="submit">提交</v-btn>
              </v-form>
              <v-card-actions>
                <v-btn class="text-white mb-3" variant="tonal" @click="tjdialog = false"
                  >关闭</v-btn
                >
              </v-card-actions>
            </v-card>
          </v-card>
        </v-dialog>
      </v-btn>
    </v-card-actions>
  </v-card>
  <!-- 首页海洋主题的“认识欧穆云”结束 -->

  <!-- 首页light主题的“认识欧穆云”开始 -->
  <v-card
    v-else
    class="mx-auto px-2 pt-4 pb-8 rounded-0"
    prepend-icon="mdi-vuetify"
    append-icon="mdi-electron-framework"
    title="认识OuMuCloud"
    subtitle="以强大的业务能力服务客户"
    color="blue-lighten-1"
    variant="tonal"
  >
    <v-card
      class="mx-auto my-3 px-4 py-3 rounded-lg"
      width="100%"
      prepend-icon="mdi-microsoft-teams"
      append-icon="mdi-compass-rose"
      title="关于团队"
      subtitle="实现客户的需求是我们矢志不渝的使命"
      color="blue-lighten-1"
      hover
      variant="outlined"
      >徐州欧穆云软件科技合伙企业（普通合伙）提供全面的质优价廉的专业软件外包服务
      <br />
      企业技术栈丰富，适用于各种业务（H5网站，移动APP,小程序，微信公众号，桌面应用，爬虫等等）,我们有充分的实力与信心实现客户需求。<br />
      企业所有技术人员均为全栈工程师，技术水平成熟，拥有丰富的项目开发，维护，团队协作的相关经验，使用github
      teams,replit teams相互配合，共同高质量的完成项目并快速交付。<br />
      我们贯彻坚守"客户至上"的原则，以客户利益为根本出发点和落脚点，全心全意为客户服务，始终把客户利益放在第一位，尽全力确保快速无误地交付令客户满意的高质量项目。<br />
    </v-card>

    <v-card
      class="mx-auto my-3 px-4 py-3 rounded-lg"
      width="100%"
      prepend-icon="mdi-microsoft-dynamics-365"
      append-icon="mdi-lightning-bolt-outline"
      title="丰富的技术栈"
      subtitle="客户自由选择项目技术栈"
      hover
      variant="outlined"
      color="indigo-accent-1"
      >客户可在我们能力范围内自由选择技术栈进行项目开发<br />
      对于APP,可选Flutter/uniapp跨平台开发安卓/IOS两端，或kotlin与swift分别原生开发<br />
      对于桌面应用，可用electron/Qt快速开发跨平台（Windows,MacOS,linux）桌面应用<br />
      对于小程序，我们通常用uniapp多端平台快速部署小程序。<br />
      对于网站，我们支持客户自由选择前后端技术栈，数据库与UI框架<br />
      目前前后端框架支持vue3+springboot/thinkPHP/Flask。数据库支持MySQL
      <br />
      CSS框架优先支持vuetify,其次是LayUI,vant,ElementUI,Tailwind
      <br />
    </v-card>

    <v-card
      class="mx-auto my-3 px-4 py-3 mb-5 rounded-lg"
      width="100%"
      prepend-icon="mdi-cube-scan"
      append-icon="mdi-klingon"
      title="扩展业务"
      subtitle="更多的扩展业务等您探索"
      hover
      variant="outlined"
      color="indigo-accent-2"
      >web:爬取海量资源/数据（合法范围内） <br />
      UI设计:助力构建精美现代化UI界面/logo/图标等 <br />
      云服务:高配低价的网站托管/云存储服务 <br />
    </v-card>

    <!-- 对话框面板 -->
    <v-card-actions>
      <v-btn rounded="lg" elevation="4" append-icon="mdi-chevron-double-up"
        >服务列表
        <v-dialog
          v-model="fwdialog"
          :scrim="false"
          transition="dialog-bottom-transition"
          activator="parent"
          fullscreen
        >
          <v-card
            class="bg-white text-blue mx-auto pa-2 rounded-lg"
            style="height: 100%; opacity: 0.9"
            width="100%"
            prepend-icon="mdi-storefront-plus-outline"
            append-icon="mdi-cart-plus"
            title="服务列表"
            subtitle="我们要为您提供哪些服务呢"
          >
            <v-expansion-panels class="mt-3" multiple="true" variant="accordion">
              <v-expansion-panel
                class="text-blue-lighten-1"
                color="blue"
                rounded="lg"
                title="安卓与IOS移动应用APP原生开发"
                text="使用Flutter开发跨平台移动应用，效果极其贴近原生，高质量开发，快速交付"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-blue-lighten-1"
                color="blue"
                rounded="lg"
                title="多端小程序与微信公众号开发与上线"
                text="用uniapp等技术开发多端小程序，包含微信，QQ，支付宝，抖音，百度等各大平台"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-blue-lighten-1"
                color="blue"
                rounded="lg"
                title="优质网站设计,开发与部署,外包与定制服务"
                text="使用vue3+springboot+MySQL等技术组合开发响应式自适应网站，完美适配各种设备"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-blue-lighten-1"
                color="blue"
                rounded="lg"
                title="跨平台（win,linux,macOS）桌面应用开发"
                text="Qt或electron开发跨平台桌面应用，涵盖Windows,Linux,MacOS"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-blue-lighten-1"
                color="blue"
                rounded="lg"
                title="智能硬件嵌入式系统专业外包服务"
                text="Linux+stm32+C+Qt开发嵌入式系统与现代上位机程序"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-blue-lighten-1"
                color="blue"
                rounded="lg"
                title="针对网站，各类应用的现代化精美UI设计"
                text="使用先进UI设计工具，打造精妙绝伦的现代化用户界面"
              >
              </v-expansion-panel>
              <v-expansion-panel
                class="text-blue-lighten-1"
                color="blue"
                rounded="lg"
                title="网站托管，云存储等各种优质云服务"
                text="配置优，性能好，价格低，速度快，轻管控，售后服务到位的欧穆云"
              >
              </v-expansion-panel>
            </v-expansion-panels>
            <v-card-actions>
              <v-btn
                class="font-weight-bold"
                rounded="lg"
                elevation="1"
                append-icon="mdi-chevron-down"
                color="blue"
                variant="tonal"
                @click="fwdialog = false"
                >关闭</v-btn
              >
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-btn>
      <v-btn rounded="lg" elevation="4" append-icon="mdi-chevron-double-up"
        >提交需求
        <v-dialog
          v-model="tjdialog"
          fullscreen
          :scrim="false"
          transition="dialog-bottom-transition"
          activator="parent"
          width="100%"
        >
          <v-card
            style="opacity: 0.97"
            class="bg-white text-blue mx-auto px-3 pt-2 rounded-lg"
            width="100%"
            prepend-icon="mdi-puzzle-heart-outline"
            append-icon="mdi-notebook-heart"
            title="提交需求"
            subtitle="我们一定全力以赴完成"
          >
            <v-card elevation="2" class="px-4 pt-3 mt-3">
              <v-form @submit.prevent>
                <v-text-field
                  class="text-blue"
                  prepend-inner-icon="mdi-card-account-details-star-outline"
                  append-inner-icon="mdi-tag-multiple-outline"
                  clearable
                  label="怎么称呼?"
                  hint="虚拟姓氏也可以，仅为方便称呼您"
                  density="compact"
                >
                </v-text-field>
                <v-text-field
                  class="text-blue"
                  prepend-inner-icon="mdi-phone-message-outline"
                  counter="13"
                  append-inner-icon="mdi-cellphone-message"
                  label="邮箱/手机号/QQ/微信/telegram/signal 等等"
                  hint="优先支持手机/QQ"
                  placeholder="1778607946@qq.com"
                  type="email"
                  clearable
                  density="compact"
                ></v-text-field>
                <v-textarea
                  prepend-inner-icon="mdi-account-circle"
                  append-inner-icon="mdi-email-heart-outline"
                  label="需求描述"
                  placeholder="描述一下您的具体需求，或在下方上传需求文档"
                  hint="尽量上传需求文档或详细描述需求"
                  clearable
                  class="text-blue"
                  density="compact"
                ></v-textarea>
                <v-file-input
                  clearable
                  label="上传需求文档"
                  hint="建议尽量上传"
                  variant="outlined"
                  class="text-blue"
                  density="compact"
                ></v-file-input>

                <v-range-slider
                  label="预算:"
                  thumb-label="always"
                  v-model="range"
                  tick-size="3"
                  track-color="blue-lighten-3"
                  track-fill-color="blue-lighten-1"
                  show-ticks="always"
                  strict
                  :min="100"
                  :max="1000000"
                  hint="可手动输入"
                  density="compact"
                >
                  <template v-slot:prepend>
                    <v-text-field
                      style="width: 91px"
                      class="text-blue"
                      v-model="range[0]"
                      hide-details
                      single-line
                      type="number"
                      variant="outlined"
                      density="compact"
                    ></v-text-field>
                  </template>

                  <template v-slot:append>
                    <v-text-field
                      style="width: 91px"
                      color="blue"
                      class="text-blue"
                      v-model="range[1]"
                      hide-details
                      single-line
                      type="number"
                      variant="outlined"
                      density="compact"
                    ></v-text-field>
                  </template>
                </v-range-slider>

                <v-select
                  class="text-blue"
                  clearable
                  chips
                  lable="项目类型"
                  item-color="blue"
                  :items="[
                    'APP',
                    '小程序',
                    '网站',
                    '桌面应用',
                    '嵌入式',
                    '爬虫',
                    'UI设计',
                    '其他',
                  ]"
                  multiple
                  variant="outlined"
                  hint="可多选"
                  placeholder="APP/小程序/网站/桌面应用"
                  density="compact"
                ></v-select>
                <v-switch
                  color="info"
                  class="text-blue"
                  v-model="model"
                  hide-details
                  inset
                  density="compact"
                  true-value="接受"
                  false-value="不接受"
                  :label="`是否接受定金: ${model.toString()}`"
                ></v-switch>
                <v-btn class="ml-2 mt-3 text-blue" type="submit">提交</v-btn>
              </v-form>
              <v-card-actions>
                <v-btn class="text-blue my-3" variant="tonal" @click="tjdialog = false"
                  >关闭</v-btn
                >
              </v-card-actions>
            </v-card>
          </v-card>
        </v-dialog>
      </v-btn>
    </v-card-actions>
  </v-card>
  <!-- 首页light主题的“认识欧穆云”结束 -->

  <!-- 首页海洋主题的联系方式开始 -->
  <v-card
    v-if="theme.global.current.value.dark"
    style="background-color: #161616"
    class="mx-auto pa-4 pb-10 rounded-0 text-blue-lighten-2"
    prepend-icon="mdi-odnoklassniki"
    append-icon="mdi-access-point-plus"
    title="联系方式"
    subtitle="交个朋友吧"
  >
    <v-alert
      density="compact"
      title="手机号"
      border="start"
      value="true"
      class="bg-black text-indigo-accent-1 mb-4 px-6 py-5"
      icon="mdi-phone-dial-outline"
    >
      18952131771
    </v-alert>
    <v-alert
      density="compact"
      title="微信"
      border="start"
      value="true"
      class="bg-black text-indigo-accent-1 my-4 px-6 py-5"
      icon="mdi-wechat"
    >
      gemolin66
    </v-alert>
    <v-alert
      density="compact"
      title="QQ"
      border="start"
      value="true"
      class="bg-black text-indigo-accent-1 my-4 px-6 py-5"
      icon="mdi-qqchat"
    >
      <ul density="compact">
        <li class="rounded-t-lg py-3">• 1778607946</li>
        <li class="py-3">• 2772222271</li>
        <li class="py-3">• 2418343672</li>
        <li class="rounded-b-lg py-3">• 1726024629</li>
      </ul>
    </v-alert>

    <v-alert
      density="compact"
      title="邮箱"
      border="start"
      value="true"
      class="bg-black text-indigo-accent-1 mt-4 px-6 py-5"
      icon="mdi-microsoft-outlook"
    >
      <ul density="compact">
        <li class="rounded-t-lg py-4">outlook邮箱 ： tzgemolin@outlook.com</li>
        <li class="py-3">QQ邮箱 ： 1778607946@qq.com</li>
        <li class="rounded-b-lg py-3">189邮箱 ： 18952131770@189.cn</li>
      </ul>
    </v-alert>
  </v-card>

  <!-- 首页海洋主题的联系方式结束 -->

  <!-- 首页light主题的联系方式开始 -->

  <v-card
    v-else
    class="mx-auto px-2 pt-4 pb-12 rounded-0"
    prepend-icon="mdi-odnoklassniki"
    append-icon="mdi-access-point-plus"
    title="联系方式"
    subtitle="交个朋友吧"
    color="blue-lighten-1"
    variant="tonal"
  >
    <v-alert
      density="compact"
      title="手机号"
      border="start"
      value="true"
      class="bg-white text-indigo-accent-1 mb-4 px-6 py-5"
      icon="mdi-phone-dial-outline"
    >
      18952131771
    </v-alert>
    <v-alert
      density="compact"
      title="微信"
      border="end"
      value="true"
      class="my-4 px-6 py-5"
      icon="mdi-wechat"
      color="indigo-accent-1"
      variant="tonal"
    >
      gemolin66
    </v-alert>
    <v-alert
      density="compact"
      title="QQ"
      border="start"
      value="true"
      class="bg-white text-indigo-accent-1 my-4 px-6 py-5"
      icon="mdi-qqchat"
    >
      <ul density="compact">
        <li class="rounded-t-lg py-3">• 1778607946</li>
        <li class="py-3">• 2772222271</li>
        <li class="py-3">• 2418343672</li>
        <li class="rounded-b-lg py-3">• 1726024629</li>
      </ul>
    </v-alert>

    <v-alert
      density="compact"
      title="邮箱"
      border="end"
      value="true"
      class="mt-4 px-6 py-5"
      color="indigo-accent-1"
      variant="tonal"
      icon="mdi-microsoft-outlook"
    >
      <ul density="compact">
        <li class="rounded-t-lg py-4">outlook邮箱 ： tzgemolin@outlook.com</li>
        <li class="py-3">QQ邮箱 ： 1778607946@qq.com</li>
        <li class="rounded-b-lg py-3">189邮箱 ： 18952131770@189.cn</li>
      </ul>
    </v-alert>
  </v-card>
  <!-- 首页light主题的联系方式结束 -->

  <!-- 首页海洋主题脚注开始 -->
  <v-footer
    v-if="theme.global.current.value.dark"
    style="background: linear-gradient(#161616, 30%, rgb(0, 10, 70)); opacity: 1"
    height="100%"
    class="text-medium-emphasis text-center d-flex flex-column"
  >
    <div class="py-8 fonsi">
      <p style="line-height: 28.5px">
        2025 |徐州欧穆云软件科技合伙企业（普通合伙）©版权所有
      </p>
      <p style="line-height: 28.5px">
        <img src="../assets/beian.png" style="vertical-align: text-bottom" />
        苏公网安备31890805607697号 | 苏ICP备1504646号-1
        <br />
      </p>
      <p style="line-height: 28.5px">地址：徐州市鼓楼区金山桥三环东路E20创意园A栋六楼</p>
      <p style="line-height: 28.5px">服务政策 | 加入我们 | 联系我们</p>
      <p style="line-height: 28.5px">电话：021-18952131771|传真:021-72342355</p>
      <p style="line-height: 28.5px">企业临时负责人：葛墨林</p>
    </div>
  </v-footer>
  <!-- 首页海洋主题脚注结束 -->

  <!-- 首页light主题脚注开始 -->
  <v-footer
    v-else
    style="background: linear-gradient(#e8f4fd, 40%, #3d77ff); opacity: 0.9"
    height="100%"
    class="text-medium-emphasis text-center d-flex flex-column touming"
  >
    <div class="py-8 fonsi">
      <p style="line-height: 28.5px">
        2025 |徐州欧穆云软件科技合伙企业（普通合伙）©版权所有
      </p>
      <p style="line-height: 28.5px">
        <img src="../assets/beian.png" style="vertical-align: text-bottom" />
        苏公网安备31890805607697号 | 苏ICP备1504646号-1
        <br />
      </p>
      <p style="line-height: 28.5px">地址：徐州市鼓楼区金山桥三环东路E20创意园A栋六楼</p>
      <p style="line-height: 28.5px">服务政策 | 加入我们 | 联系我们</p>
      <p style="line-height: 28.5px">电话：021-18952131771|传真:021-72342355</p>
      <p style="line-height: 28.5px">企业临时负责人：葛墨林</p>
    </div>
  </v-footer>
  <!-- 首页light主题脚注结束 -->
</template>

<script setup>
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
    fwdialog: false,
    tjdialog: false,
    notifications: false,
    sound: true,
    widgets: false,
    model: true,
  }),
};
</script>

<style lang="scss" scoped></style>

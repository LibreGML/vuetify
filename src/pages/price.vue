<template>
  <v-banner
    class="text-indigo-accent-1"
    icon="mdi-email-alert-outline"
    lines="three"
    stacked
  >
    <v-banner-text>
      云服务目前尚未开放，将在不久后推出，以下只是部分机型的未来定价参考，更多机型定价标准陆续推出中。<br />
      推出之后，在此页面会开通下单渠道，选择对应机型下单后即可获得对应服务器公网IP+root用户名以及密码
      <br />
      关于具体使用，如ssh登录，宝塔面板，文件管理等等可加本站左上方葛墨林QQ：
      1778607946直接询问。
      <br />
    </v-banner-text>
    <template v-slot:actions>
      <v-btn color="light-blue-accent-2">谢谢您的支持～</v-btn>
    </template>
  </v-banner>
  <v-table fixed-header hover height="600px">
    <thead class="text-body-1 text-indigo-accent-1">
      <tr>
        <th class="text-center">名称</th>
        <th class="text-center">配置</th>
        <th class="text-center">定价</th>
        <th class="text-center">期限</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="item in desserts" :key="item.name">
        <td class="text-center">{{ item.name }}</td>
        <td class="text-center">{{ item.tip }}</td>
        <td class="text-center">{{ item.calories }}</td>
        <td class="text-center">{{ item.time }}</td>
      </tr>
    </tbody>
  </v-table>
  <v-divider :thickness="4" color="indigo-accent-1" class="border-opacity-25"></v-divider>

  <v-card
    class="mx-auto my-10 px-3 pt-2 rounded-lg"
    width="100%"
    height="100%"
    prepend-icon="mdi-file-upload"
    append-icon="mdi-form-select"
    title="提交需求"
    subtitle="我们一定全力以赴完成"
  >
    <v-card elevation="1" class="px-4 pt-5 mt-3 pb-5">
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
        <v-radio-group
          class="text-indigo-accent-1"
          inline
          label="方便询问您的性别吗?"
          hint="仅用于方便称呼"
          density="compact"
        >
          <v-radio label="男" value="男"></v-radio>
          <v-radio label="女" value="女"></v-radio>
          <v-radio label="不透漏" value="不透漏"></v-radio>
        </v-radio-group>

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
          class="text-indigo-accent-1"
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

        <v-select
          class="text-indigo-accent-1"
          clearable
          chips
          lable="设备类型"
          item-color="indigo-accent-1"
          :items="[
            '云服务器',
            'CDN',
            'VPN',
            'AnyCast',
            '数据库',
            '云存储',
            '云托管',
            '其他',
          ]"
          multiple
          variant="outlined"
          hint="可多选"
          placeholder="云托管/云存储/云计算/公网加速"
          density="compact"
        ></v-select>
        <v-btn class="ml-2 mt-4 text-blue" type="submit">提交</v-btn>
      </v-form>
    </v-card>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    model: true,
    // 设备定价模块的表单数据
    desserts: [
      {
        name: "国内特惠年费机1",
        calories: "￥50/年",
        tip: "2核 4G运存 40G存储 无限流量 带宽10Mbps",
        time: "年",
      },
      {
        name: "国内特惠年费机2",
        calories: "￥80/年",
        tip: "4核 8G运存 40G存储 无限流量 带宽10Mbps",
        time: "年",
      },
      {
        name: "共享1号机",
        calories: "￥6.00",
        tip: "多人 8核 32G运存 20G硬盘 30M带宽 ",
        time: "终身",
      },
      {
        name: "共享2号机",
        calories: "￥6/月",
        tip: "多人 12核 64G运存 80G硬盘 30M带宽",
        time: "月",
      },
      {
        name: "体验款VPS",
        calories: "￥9.9",
        tip: "1核 1G运存 30G存储 带宽5M",
        time: "月",
      },
      {
        name: "入门级VPS",
        calories: "￥13/年",
        tip: "1核 2G运存 30G存储 带宽10M",
        time: "年",
      },
      {
        name: "MC插件小型服配置",
        calories: "￥20/年",
        tip: "1核 4G运存 30G存储 带宽10M",
        time: "年",
      },
      {
        name: "MC模组服配置",
        calories: "￥24/年",
        tip: "2核 4G运存 30G存储 带宽10M",
        time: "年",
      },
      {
        name: "MC/泰拉开服配置",
        calories: "￥50/年",
        tip: "3核 6G运存 30G存储 带宽10M",
        time: "年",
      },
      {
        name: "MC/泰拉多人开服配置",
        calories: "￥70/年",
        tip: "4核 8G运存 30G存储 带宽15M",
        time: "年",
      },
      {
        name: "中型服务器",
        calories: "￥170/年",
        tip: "8核 16G运存 30G存储 带宽20M",
        time: "年",
      },
      {
        name: "大型服务器",
        calories: "￥250/年",
        tip: "12核 16G运存 50G存储 带宽50M",
        time: "年",
      },
      {
        name: "PPTP服务器",
        calories: "￥50/年",
        tip: "4核 8G运存 10G存储 带宽20M",
        time: "年",
      },
      {
        name: "P2TP服务器",
        calories: "￥50/年",
        tip: "4核 8G运存 10G存储 带宽20M",
        time: "年",
      },
    ],
  }),
};
</script>

<style lang="scss" scoped></style>

<script setup lang="ts">
import logo from '@/assets/logo.svg?raw';
import { VerticalNavLink, VerticalNavSectionTitle } from '@layouts';
import { useTheme } from 'vuetify';
const vuetifyTheme = useTheme()
</script>

<template>
  <!-- 👉 Nav header -->
  <div class="nav-header">
    <RouterLink
      to="/"
      class="app-logo d-flex align-center gap-x-3 app-title-wrapper"
    >
      <!-- ℹ️ You can also use img tag or VImg here -->
      <div v-html="logo" />

      <Transition name="vertical-nav-app-title">
        <h1 class="font-weight-semibold leading-normal text-xl">
          NAStool
        </h1>
      </Transition>
    </RouterLink>
  </div>

  <!-- 👉 Nav items -->
  <ul>
    <VerticalNavLink
      :item="{
        title: '开始',
        to: 'index',
        icon: { icon: 'mdi-home-outline' },
      }"
    />
    <!-- 👉 资源 -->
    <VerticalNavSectionTitle :item="{ heading: '资源' }" />
    <VerticalNavLink
      :item="{
        title: '资源搜索',
        to: '',
        icon: { icon: 'mdi-magnify' },
      }"
    />
    <VerticalNavLink
      :item="{
        title: '推荐',
        to: 'card-basic',
        icon: { icon: 'mdi-star-outline' },
      }"
    />

    <!-- 👉 站点 & 订阅 -->
    <VerticalNavSectionTitle :item="{ heading: '站点 & 订阅' }" />

    <VerticalNavLink
      :item="{
        title: '站点管理',
        to: '',
        icon: { icon: 'mdi-sitemap-outline' },
      }"
    />
    <VerticalNavLink
      :item="{
        title: '订阅管理',
        to: '',
        icon: { icon: 'mdi-list-box-outline' },
      }"
    />
    
    <!-- 👉 下载 & 整理 -->
    <VerticalNavSectionTitle :item="{ heading: '下载 & 整理' }" />
    <VerticalNavLink
      :item="{
        title: '下载管理',
        to: '',
        icon: { icon: 'mdi-tray-arrow-down' },
      }"
    />
    <VerticalNavLink
      :item="{
        title: '媒体整理',
        to: '',
        icon: { icon: 'mdi-movie-cog-outline' },
      }"
    />

    <!-- 👉 系统 -->
    <VerticalNavSectionTitle :item="{ heading: '系统' }" />
    <VerticalNavLink
      :item="{
        title: '服务',
        to: '',
        icon: { icon: 'mdi-apps' },
      }"
    />
    <VerticalNavLink
      :item="{
        title: '基础设置',
        to: 'account-settings',
        icon: { icon: 'mdi-cog-outline' },
      }"
    />
    <VerticalNavLink
      :item="{
        title: '进阶设置',
        to: '',
        icon: { icon: 'mdi-account-cog-outline' },
      }"
    />
  </ul>
</template>

<style lang="scss">
// .v-navigation-drawer {
//   height: 100%;

//   .v-navigation-drawer__content {
//     display: flex;
//     flex-direction: column;

//     > ul {
//       flex-grow: 1;
//     }
//   }
// }

.upgrade-banner {
  margin-top: auto;
  // position: absolute;
  // bottom: 13px;
  // left: 50%;
  // transform: translateX(-50%);
}
</style>

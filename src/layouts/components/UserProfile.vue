<script setup lang="ts">
import avatar1 from '@/assets/images/avatars/avatar-1.png';
import type { Anchor } from 'vuetify/lib/components';

const avatarBadgeProps = {
  dot: true,
  location: 'bottom right' as Anchor,
  offsetX: 3,
  offsetY: 3,
  color: 'success',
  bordered: true,
}
</script>

<template>
  <VBadge v-bind="avatarBadgeProps">
    <VAvatar
      style="cursor: pointer;"
      color="primary"
      variant="tonal"
    >
      <VImg :src="avatar1" />

      <!-- SECTION Menu -->
      <VMenu
        activator="parent"
        width="230"
        location="bottom end"
        offset="14px"
      >
        <VList>
          <!-- 👉 User Avatar & Name -->
          <VListItem>
            <template #prepend>
              <VListItemAction start>
                <VBadge v-bind="avatarBadgeProps">
                  <VAvatar
                    color="primary"
                    size="40"
                    variant="tonal"
                  >
                    <VImg :src="avatar1" />
                  </VAvatar>
                </VBadge>
              </VListItemAction>
            </template>

            <VListItemTitle class="font-weight-semibold">
              admin
            </VListItemTitle>
            <VListItemSubtitle class="text-disabled">
              管理员
            </VListItemSubtitle>
          </VListItem>

          <VDivider class="my-2" />

          <!-- 👉 Pricing -->
          <VListItem link>
            <template #prepend>
              <VIcon
                class="me-2"
                icon="mdi-message-outline"
                size="22"
              />
            </template>

            <VListItemTitle>消息中心</VListItemTitle>
          </VListItem>

          <!-- 👉 FAQ -->
          <VListItem link>
            <template #prepend>
              <VIcon
                class="me-2"
                icon="mdi-text-box-outline"
                size="22"
              />
            </template>

            <VListItemTitle>实时日志</VListItemTitle>
          </VListItem>

          <!-- Divider -->
          <VDivider class="my-2" />

          <VListItem to="/">
            <template #prepend>
              <VIcon
                class="me-2"
                icon="mdi-restart-alert"
                size="22"
              />
            </template>

            <VListItemTitle>重启</VListItemTitle>
          </VListItem>

          <VListItem to="/">
            <template #prepend>
              <VIcon
                class="me-2"
                icon="mdi-update"
                size="22"
              />
            </template>

            <VListItemTitle>更新</VListItemTitle>
          </VListItem>

          <!-- 👉 Logout -->
          <VListItem to="/login">
            <template #prepend>
              <VIcon
                class="me-2"
                icon="mdi-logout-variant"
                size="22"
              />
            </template>

            <VListItemTitle>注销</VListItemTitle>
          </VListItem>
        </VList>
      </VMenu>
      <!-- !SECTION -->
    </VAvatar>
  </VBadge>
</template>

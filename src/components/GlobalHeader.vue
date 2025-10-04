<template>
  <div id="globalHeader">
    <a-menu v-model:selectedKeys="current" mode="horizontal" :items="items" />
  </div>
</template>
<script lang="ts" setup>
import { h, ref } from 'vue';
import { MailOutlined, HomeOutlined, SettingOutlined } from '@ant-design/icons-vue';
import { MenuProps } from 'ant-design-vue';
const current = ref<string[]>(['mail']);
const items = ref<MenuProps['items']>([
  {
    key: '/',
    icon: () => h(HomeOutlined),
    label: '主页l',
    title: '主页t',
  },
  {
    key: '/user/login',
    icon: () => h(MailOutlined),
    label: '登录l',
    title: '登录t',
  },
  {
    key: '/user/register',
    icon: () => h(SettingOutlined),
    label: '注册l',
    title: '注册t',
    children: [
      {
        type: 'group',
        label: 'Item 1',
        children: [
          {
            label: 'Option 1',
            key: 'setting:1',
          },
          {
            label: 'Option 2',
            key: 'setting:2',
          },
        ],
      },
      {
        type: 'group',
        label: 'Item 2',
        children: [
          {
            label: 'Option 3',
            key: 'setting:3',
          },
          {
            label: 'Option 4',
            key: 'setting:4',
          },
        ],
      },
    ],
  },
  {
    key: 'alipay',
    label: h(
      'a', 
      { href: 'https://antdv.com', target: '_blank' }, '听说这是个跳转网页的链接'),
    title: '听说这是个跳转网页的标题',
  },
]);
</script>


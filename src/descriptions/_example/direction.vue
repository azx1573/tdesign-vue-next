<template>
  <t-space direction="vertical">
    <t-row>
      <span>整体布局：</span>
      <t-radio-group v-model="layout" :options="layoutOptions"></t-radio-group>
    </t-row>

    <t-row>
      <span>item布局：</span>
      <t-radio-group v-model="itemLayout" :options="itemLayoutOptions"></t-radio-group>
    </t-row>

    <t-descriptions title="Shipping address" bordered :layout="layout" :item-layout="itemLayout" :column="3">
      <t-descriptions-item label="Name">TDesign</t-descriptions-item>
      <t-descriptions-item label="Telephone Number">139****0609</t-descriptions-item>
      <t-descriptions-item label="Area">China Tencent Headquarters</t-descriptions-item>
      <t-descriptions-item label="Address">Shenzhen Penguin Island D1 4A Mail Center</t-descriptions-item>
    </t-descriptions>
  </t-space>
</template>

<script setup>
import { ref } from 'vue';

const layout = ref('horizontal');
const itemLayout = ref('horizontal');

const layoutOptions = ['horizontal', 'vertical'];
const itemLayoutOptions = ['horizontal', 'vertical'];
</script>

<template>
  <PanelTemplate value="Donate" class="donate-container">
    <h2 class="text-2xl font-bold mb-2">
      {{ $t('g.donate') }}
    </h2>
    <p class="mb-4">{{ $t('g.donateMessage') }}</p>

    <div class="flex gap-4">
      <div>
        <h3 class="text-lg font-semibold mb-2">Alipay</h3>
        <img src="/assets/alipay.png" alt="Alipay QR Code" class="w-32 h-32">
      </div>
      <div>
        <h3 class="text-lg font-semibold mb-2">WeChat Pay</h3>
        <img src="/assets/wechatpay.png" alt="WeChat Pay QR Code" class="w-32 h-32">
      </div>
    </div>
  </PanelTemplate>
</template>

<script setup lang="ts">
import PanelTemplate from './PanelTemplate.vue'
</script>
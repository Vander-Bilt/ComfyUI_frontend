<template>
  <PanelTemplate value="Donate" class="donate-container">
    <h2 class="text-2xl font-bold mb-2">
      {{ $t('g.donate') }}
    </h2>
    <p class="mb-4">{{ $t('g.donateMessage1') }}</p>
    <p class="mb-4">{{ $t('g.donateMessage2') }}</p>

    <div class="flex gap-4">
      <div>
        <h3 class="text-lg font-semibold mb-2">Alipay</h3>
        
      </div>
      <div>
        <h3 class="text-lg font-semibold mb-2">WeChat Pay</h3>
        
      </div>
    </div>
  </PanelTemplate>
</template>

<script setup lang="ts">
import PanelTemplate from './PanelTemplate.vue'
</script>
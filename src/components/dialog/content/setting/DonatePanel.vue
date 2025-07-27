<template>
  <PanelTemplate value="Donate" class="donate-container">
    <h2 class="text-2xl font-bold mb-2">
      {{ $t('g.donate') }}
    </h2>
    <p class="mb-4">{{ $t('g.donateMessage1') }}</p>
    <p class="mb-4">{{ $t('g.donateMessage2') }}</p>

    <div class="mt-4">

      <div v-if="locale === 'zh'">
        <iframe id='pay_zh' :src='donateUrl' style='border:none;width:100%;padding:0px;background:#f9f9f9;' height='600' title='vanderbilt'></iframe>
      </div>
      <div v-else>
        <iframe id='kofiframe' src='https://ko-fi.com/vanderbilt/?hidefeed=true&widget=true&embed=true&preview=true' style='border:none;width:100%;padding:4px;background:#f9f9f9;' height='600' title='vanderbilt'></iframe>
      </div>

    </div>
  </PanelTemplate>
</template>

<script setup lang="ts">
import { computed } from 'vue'
import { useI18n } from 'vue-i18n'
import PanelTemplate from './PanelTemplate.vue'
import { useColorPaletteStore } from '@/stores/workspace/colorPaletteStore'

const { locale } = useI18n()
const colorPaletteStore = useColorPaletteStore()

const theme = computed(() =>
  colorPaletteStore.completedActivePalette.light_theme ? 'light' : 'dark'
)

const donateUrl = computed(() => {
  const baseUrl = 'https://donate.nav001.online/index_zh.html'
  const url = new URL(baseUrl)
  url.searchParams.append('theme', theme.value)
  return url.toString()
})
</script>
<template>
  <div class="row q-pa-md justify-center full-width-row text-no-wrap">
    <div class="col col-3 col-md-1">
      <q-img :src="`${BASE_PATH}/images/habitat-service.png`" />
    </div>
    <div class="col col-12 col-md-3">
      <div class="row q-px-md q-pt-md justify-center">
        <span class="text-h4">HABITAT SERVICE</span>
      </div>
      <div class="row q-px-md justify-center">
        <span class="text-h7">MULTISERVICES</span>
      </div>
    </div>
  </div>

  <div class="row q-py-md justify-center full-width-row">
    <template v-for="(field, index) in fields">
      <field :image-path="field.imagePath" :text="field.text" />
      <q-separator v-if="index < fields.length - 1" vertical spaced size="2px" color="grey-6" />
    </template>
  </div>

  <div class="row q-pa-md justify-center full-width-row text-no-wrap blue-top-border">
    <span class="text-h7">TRAVAUX · ÉLECTRICITÉ · AMÉNAGEMENTS</span>
  </div>
</template>

<script setup>
import Field from '@/components/Field.vue'

const BASE_PATH = import.meta.env.VITE_BASE_PATH ?? ''

const fields = [
  {
    imagePath: `${BASE_PATH}/images/light.png`,
    text: 'ÉLECTRICITÉ',
  },
  {
    imagePath: `${BASE_PATH}/images/electrical-outlet.png`,
    text: 'DÉPANAGE',
  },
  {
    imagePath: `${BASE_PATH}/images/tools.png`,
    text: 'AMÉNAGEMENTS',
  },
  {
    imagePath: `${BASE_PATH}/images/house.png`,
    text: 'MULTISERVICES',
  },
]
</script>

<style scoped>
.blue-top-border {
  border-style: solid;
  border-width: 4px 0 0 0;
  border-color: green;
}
</style>

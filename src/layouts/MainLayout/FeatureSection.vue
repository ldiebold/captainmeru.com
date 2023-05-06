<script lang="ts" setup>
interface Props {
  title: string
  img: string
  body: string
}

defineProps<Props>()
</script>

<template>
  <div class="row q-col-gutter-xl items-center">
    <h3 class="col-12 text-2.8em leading-1.4em lg:text-6em lg:leading-1.2em text-center text-grey-8 q-mb-md">
      {{ title }}
    </h3>

    <div class="col-xs-12 col-lg-7">
      <q-card class="shadow-10">
        <q-img :src="img" />
      </q-card>
    </div>

    <div
      class="col-xs-12 col-lg-5 text-2em text-grey-9"
      v-html="body"
    />
  </div>
</template>

<template>
  <q-card class="my-card col-md-3 col-sm-3 col-xs-12 text-center q-pa-lg">
    <q-avatar size="8rem">
      <q-img
        :alt="service.title"
        :src="service.img"
        :position="service.position ?? '50% 50%'"
        style="border-radius: 50%"
        width="100%"
        height="100%"
      />
    </q-avatar>
    <q-card-section>
      <div class="text-h6">{{ service.title }}</div>
    </q-card-section>
    <q-card-section class="q-pt-none">
      {{ service.description }}
    </q-card-section>
  </q-card>
</template>

<script setup>
defineProps({
  service: {
    type: Object,
    required: true,
  },
});
</script>

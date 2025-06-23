<script setup lang="ts">
const route = useRoute()
const error = route.query.error || 'Unknown error occured'
</script>

<template>
  <div class="card bg-base-300 container flex flex-col items-center justify-center gap-4 min-h-72 mt-4 mx-auto">
    <div
      role="alert"
      class="alert alert-error min-w-1/2 text-center"
    >
      <span>Oh no! {{ error }}</span>
    </div>
    <NuxtLink
      to="/"
      class="btn btn-primary"
    >
      Home
      <Icon
        name="tabler:arrow-left"
        size="32"
      />
    </NuxtLink>
  </div>
</template>

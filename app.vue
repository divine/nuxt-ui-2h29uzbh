<template>
  <UContainer class="min-h-screen flex items-center">
    <UCard
    >
      <template #header> Welcome to the playground! </template>

      <p class="text-gray-500 dark:text-gray-400">Try your components here!</p>


      <UDropdownMenu
        :items="items"
        :ui="{
          content: 'w-48'
        }"
      >
        <UButton icon="i-lucide-menu" color="neutral" variant="outline" />
      </UDropdownMenu>
    </UCard>
  </UContainer>
</template>

<script setup lang="ts">
const items = ref([
  ...[...Array(90)].map((_, index) => [{
    label: [
      'Benjamin', 'Emma', 'Lucas', 'Sophia', 'Ethan', 'Olivia', 'Noah', 'Ava',
      'Liam', 'Isabella', 'Mason', 'Mia', 'William', 'Charlotte', 'James',
      'Amelia', 'Alexander', 'Harper', 'Michael', 'Evelyn'
    ][index % 20],
    avatar: {
      alt: [
        'Benjamin', 'Emma', 'Lucas', 'Sophia', 'Ethan', 'Olivia', 'Noah', 'Ava',
        'Liam', 'Isabella', 'Mason', 'Mia', 'William', 'Charlotte', 'James',
        'Amelia', 'Alexander', 'Harper', 'Michael', 'Evelyn'
      ][index % 20]
    },
    type: 'label'
  }])
])
</script>

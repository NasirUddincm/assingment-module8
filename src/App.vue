<template>
  <div class="bg-gray-100 min-h-screen">
    <main class="max-w-3xl mx-auto p-6">
      <ParentComponent />
    </main>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  components: {
    ParentComponent,
  },
};
</script>

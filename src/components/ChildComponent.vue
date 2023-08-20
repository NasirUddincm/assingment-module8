<script setup>
  import { defineEmits } from 'vue';
  
  const props = defineProps({
    message: String,
  });
  
  const emit = defineEmits();
  
  const emitMessage = () => {
    emit('messageEmitted', 'This is Custom message from child component');
  };
</script>
  
<template>
    <div>
      <h2>Child Component</h2>
      <p>Received Message: <strong>{{ message }}</strong></p>
      <button class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded my-2"
        @click="emitMessage">
        Emit Custom Message
        </button>
    </div>
</template>
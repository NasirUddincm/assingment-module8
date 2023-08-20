
<script setup>
  import { ref } from 'vue';
  import ChildComponent from './ChildComponent.vue';
  
  const propParentMessage = ref('This Message from parent component');
  
  const emittedMessage = ref('');
  
  const handleMessageEmitted = (message) => {
    emittedMessage.value = message;
  };
</script>
  
<template>
    <div>
      <h1 class="my-3">Parent Component</h1>
      <ChildComponent :message="propParentMessage" 
                        @messageEmitted="handleMessageEmitted" />
      <p>Emitted Message: <strong>{{ emittedMessage }}</strong> </p>
    </div>
</template>
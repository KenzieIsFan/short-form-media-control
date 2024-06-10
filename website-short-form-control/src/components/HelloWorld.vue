<script setup>
import { ref } from 'vue'
defineProps({
  msg: {
    type: String,
    required: true
  }
})

const user_summary = ref('')
</script>

<template>
  <!-- Where the input will be for text input-->
  <div class="greetings">
    <h1 class="orange">{{ msg }}</h1>

    <span>Try and Write a summary of what you remember from the last video you watched:</span>
	  <p style="white-space: pre-line;">{{ user_summary }}</p>
	  <textarea v-model="user_summary" placeholder="add multiple lines"></textarea>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

textarea {
  text-align: center;
}

span {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: right;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: center;
  }
}
</style>

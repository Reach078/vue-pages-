<script setup lang="ts">
import { Button } from '@/components/ui/button';
import { Input } from '@/components/ui/input'
import { ref } from 'vue';


const userName = ref("");
const Email = ref("");
const Password = ref("");
const handleSubmit = () => {
  console.log(userName.value, Email.value, Password.value);
}
</script>

<template>
  <main>
    <h1>Testing shadcn component</h1>
    <Input v-model="userName" placeholder="Enter your Username" />
    <Input v-model="Email" placeholder="Enter your Email" />
    <Input v-model="Password" placeholder="Enter your Password" />

    <Button @click="handleSubmit">Click me</Button>
  </main>
</template>

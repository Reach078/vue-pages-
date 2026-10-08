<script setup lang="ts">
import { ref } from 'vue'

//this is a declaration of variable
//1. what user is actively typing
const firstName = ref('')
const lastName = ref('')

//2. What hold the value only after submit button is clicked
const submittedFirstName = ref('')
const submittedLastName = ref('')

//Button submit for input
const handleSubmit = () => {
  submittedFirstName.value = firstName.value
  submittedLastName.value = lastName.value
}
</script>

<template>
  <div class="flex items-center justify-center p-4">
    <div class="w-full max-w-md rounded-xl border border-border/60 bg-card p-6 shadow-sm">
      <div class="mb-6 text-center">
        <h1 class="text-2xl font-bold tracking-tight text-foreground">Welcome</h1>
        <p class="text-sm text-muted-foreground mt-1">Please enter your information below</p>
      </div>

      <form @submit.prevent="handleSubmit" class="flex flex-col gap-4">
        <div class="flex flex-col gap-1.5">
          <label class="text-sm font-medium text-foreground">First Name</label>
          <el-input
            v-model="firstName"
            placeholder="Please input your name"
            size="large"
            clearable
          />
        </div>

        <div class="flex flex-col gap-1.5">
          <label class="text-sm font-medium text-foreground">Last Name</label>
          <el-input
            v-model="lastName"
            placeholder="Please input your name"
            size="large"
            clearable
          />
          <div class="grid grid-cols-2 gap-2">
            <el-button type="primary" size="large" class="w-full mt-2" @click="handleSubmit">
              Submit
            </el-button>
            <el-button type="danger" size="large" class="w-full mt-2">Reset</el-button>
          </div>
        </div>
      </form>

      <!-- Preview value if typed -->
      <div
        v-if="firstName || lastName"
        class="mt-4 p-3 rounded-lg bg-muted/50 border border-border/40 text-center"
      >
        <span class="text-xs text-muted-foreground uppercase tracking-wider block mb-0.5"
          >Current Input</span
        >
        <span class="text-sm font-semibold text-foreground"
          >Hello User : {{ submittedFirstName }} {{ submittedLastName }}</span
        >
      </div>
    </div>
  </div>
</template>

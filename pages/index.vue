<template>
  <div class="m-10">
    <FormField
      label="Email"
      type="email"
      name="email"
      :validator="string().required('Email is required.').email('Email in invalid.')"
      :validate-on-change="true"
    />
    <FormField
      label="Full name"
      type="text"
      name="fullName"
      initial-value="Patrick Goldman"
      :validator="string().required('Full name is required.').min(5, 'Minimum of 5 characters.')"
    />
  </div>
</template>

<script lang="ts" setup>
import { string } from 'yup'
</script>

<style scoped lang="css">
</style>

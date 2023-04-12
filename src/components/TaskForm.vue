<template>
  <form @submit.prevent="handleSubmit" class="columns mt-3">
    <div class="column is-full py-2">
      <input
        class="input"
        type="text"
        placeholder="I need to..."
        v-model="newTask"
      />
    </div>
    <div class="column py-2">
      <button class="button is-warning">Add</button>
    </div>
  </form>
</template>
<script>
export default {};
</script>

<style>
</style>
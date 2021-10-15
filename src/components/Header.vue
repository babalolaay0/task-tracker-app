<template>
<header>
<h3>{{ title }}</h3>
<Button @btn-click="$emit('btn-click')" :text="closeAddTask ? 'Close' : 'Add Task'" :color="closeAddTask ? 'red' : 'green'" />
</header>
</template>

<script>
import Button from './Button'

export default {
  name: 'Header',
  props: {
    title: String,
    closeAddTask: Boolean
  },
  components: {
    Button
  }
}
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 20px;
}
</style>

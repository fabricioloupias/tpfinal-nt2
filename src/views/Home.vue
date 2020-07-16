<template>
  <div class="home">
    <FilterInput />
  </div>
</template>

<script>
// @ is an alias to /src
import FilterInput from '@/components/FilterInput.vue'

export default {
  name: 'Home',
  components: {
    FilterInput
  }
}
</script>

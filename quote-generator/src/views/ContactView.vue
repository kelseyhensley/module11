<template>
  <div class="contact">
    <h1>This is contact page</h1>
    <p>
    Email: klhensley@my.waketech.edu
    </p>
    <GoBack />
  </div>
</template>

<script>
import GoBack from '@/components/GoBack.vue'

export default {
  name: 'ContactView',
  components: {
    GoBack
  }
}
</script>
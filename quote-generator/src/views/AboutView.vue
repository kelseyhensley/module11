<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>
    Hi, my name is Kelsey! I am almost 
    28 years old and I am in the Web & UX Design
    program at Wake Tech. I enjoy crocheting and
    playing the piano. I also have two dogs and two cats
    that I love very much. 
    </p>
    <GoBack />
  </div>
</template>

<script>
import GoBack from '@/components/GoBack.vue'

export default {
  name: 'AboutView',
  components: {
    GoBack
  }
}
</script>
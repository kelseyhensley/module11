<template>
  <div class="quotes">
    <h1>Random Quote Generator</h1>

    <!-- Display the quote or a loading message -->
    <p v-if="loading">Loading...</p>
    <p v-else>"{{ quote }}"</p>
    <p class="author">— {{ author }}</p>
    <!-- The button that triggers the API call -->
    <button @click="getQuote">Get New Quote</button>

    <br>
    <GoBack />

  </div>
</template>

<script>
// @ is an alias to /src
import axios from 'axios'
import GoBack from '@/components/GoBack.vue'

export default {
  name: 'QuotesView',
  components: {
    GoBack
  },

    data() {
      return {
        quote: '',      // stores the quote text
        author: '', // stores the author text
        loading: false  // tracks loading status
      }
    },
  methods: {
    async getQuote() {
      this.loading = true
      try {
        // Send a GET request to the Quotable API
const response = await axios.get(
  'https://quotes15.p.rapidapi.com/quotes/random/?language_code=en',
  {
    headers: {
      'x-rapidapi-host': 'quotes15.p.rapidapi.com',
      'x-rapidapi-key': '90ca4aa305msh5a6e06565e3fd1dp1ae828jsn5be2f81b487e'
    }
  }
)  
// Update the quote with the response data
         this.quote = response.data.content
         this.author = response.data.originator.name
      } catch (error) {
        console.error('Error fetching quote:', error)
        this.quote = 'Oops! Something went wrong.'
        this.author = ''
      } finally {
        this.loading = false
      }
    }
  },
  mounted() {
    // Load a random quote when the app first starts
    this.getQuote()
  }


}
</script>

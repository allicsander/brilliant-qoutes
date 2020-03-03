<template>
    <div class="container">
      <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
import QuoteGrid from './components/QuotesGrid.vue';

    export default {
        data() {
          return{
              quotes: ['be sexy'],
              maxQoutes: 10
          } 
        
        },
        components:{
          appQuoteGrid: QuoteGrid
        }

    }
</script>

<style>
</style>

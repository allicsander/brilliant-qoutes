<template>
    <div class="container">
      <app-new-quote @quoteAdded="newQuote"></app-new-quote>
      <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
import QuoteGrid from './components/QuotesGrid.vue';
import NewQuote from './components/NewQuote.vue';

    export default {
        data() {
          return{
              quotes: ['be sexy', 'be strong'],
              maxQoutes: 10
          } 
        
        },
        methods:{
          newQuote(quote){
            this.quotes.push(quote);
          }
        },
        components:{
          appQuoteGrid: QuoteGrid,
          appNewQuote: NewQuote
        }

    }
</script>

<style>
</style>

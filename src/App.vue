<template>
    <div class="container">
      <app-new-quote @quoteAdded="newQuote"></app-new-quote>
      <app-quote-grid :quotes="quotes" @quoteDeleted="deleteBrilliantQuote"></app-quote-grid>
      <div class="rom">
        <div class="col-sm-12 text-center">
          <div class="alert alert-info">
            tip: click on a quote to delete it
          </div>
        </div>
      </div>
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
          },
          deleteBrilliantQuote(index){
            this.quotes.splice(index, 1);
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

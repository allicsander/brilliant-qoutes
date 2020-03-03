<template>
    <div class="container">
      <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
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
import Header from './components/Header.vue';

    export default {
        data() {
          return{
              quotes: ['be sexy', 'be strong'],
              maxQuotes: 10
          } 
        
        },
        methods:{
          newQuote(quote){
            if(this.quotes.length < 10){
              this.quotes.push(quote);
            }
          },
          deleteBrilliantQuote(index){
            this.quotes.splice(index, 1);
          }
        },
        components:{
          appQuoteGrid: QuoteGrid,
          appNewQuote: NewQuote,
          appHeader: Header
        }

    }
</script>

<style>
</style>

<template>


    <div class="col-md-12">
       <app-quote v-for="(quote, index) in quotes" :index = "index" :quotes = "quotes">
           <p>{{ quote }}</p>
       </app-quote>
    </div>


</template>




<script>

    import appQuote from './quote.vue';
    export default {
        props: {
          quotes: Array
        },
        components: {
            appQuote: appQuote
        }
    }

</script>
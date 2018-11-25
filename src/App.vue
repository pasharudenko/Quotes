<template>
    <div class="container">
        <div class="row">
            <app-progress :quotes = "quotes"></app-progress>
            <app-form :quotes = "quotes"></app-form>
            <app-quote-container :quotes = "quotes"></app-quote-container>
        </div>
    </div>
</template>

<script>
    import appProgress from './components/progress-bar.vue';
    import appForm from './components/form.vue';
    import appQuoteContainer from './components/quote-container.vue';
    export default {
        data() {
          return {
              quotes: [],
          }
        },
        components: {
            appProgress: appProgress,
            appForm: appForm,
            appQuoteContainer: appQuoteContainer
        }
    }
</script>


<style>
    .panel-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: #6e6e6e;
    }
    .quote {
        cursor: pointer;
    }
    .quote:hover {
        background-color: #ffe2e2;
    }
</style>

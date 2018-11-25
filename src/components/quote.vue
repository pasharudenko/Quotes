<template>


    <div class="panel panel-body quote" @click="deleteItem">
       <slot></slot>
    </div>


</template>

<script>

    export default {
        props: {
            index: Number,
            quotes: Array,
        },
        methods: {
            deleteItem() {
                this.quotes.splice(this.index, 1);
            }
        }
    }

</script>

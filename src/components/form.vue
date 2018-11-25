<template>


    <form>
        <div class="form-group">
            <label for="message">Message</label>
            <textarea id="message" rows="3" class="form-control" v-model="message"></textarea>
        </div>
        <button type="submit" class="btn btn-primary" @click="addQuote">Submit</button>
    </form>


</template>


<script>
    export default {
        props: {
            quotes: Array
        },
        data() {
            return {
                message: '',
            }
        },
        methods: {
            addQuote() {
                event.preventDefault();
                if(this.quotes.length <= 9) {
                    this.quotes.push(this.message);
                    this.message = '';
                } else {
                    alert('Max limit of quotes');
                }


            }
        }
    }
</script>
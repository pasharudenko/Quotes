<template>
    <div>
        <h1>Quotes added</h1>
        <div class="progress">
            <div style="height: 20px;" :style="{width: progress}" class="progress-bar">{{ progress }}</div>
        </div>
    </div>
</template>

<script>

    export default {
        props: {
            quotes: Array
        },
        computed: {
            progress() {
                return this.quotes.length * 10 + '%';
            }
        }
    }

</script>
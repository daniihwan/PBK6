<script>
export default {
    props: ["callback"],
    methods: {
        sendMessage() {
            const message = "halo dari child component";
            this.callback(message);
        },
    },
},
</script>

<template>
<div class="child">
    <h2>Child Component</h2>
    <button> @click="sendMessage"> kirim Data ke Parent</button>
</div>
</template>

<style>

</style>
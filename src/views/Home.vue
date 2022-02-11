<template>

<div class="container">
    <h1>Home</h1>
</div>

<div class="container">
    <Chat />
</div>
    
</template>

<script>
import Chat from '../components/Chat.vue'

export default {
    name: "Home",
    
    data() {
        return {
            data: "",
        }
    },
    components: {
        Chat,
    },

    computed: {

    },

    methods: {

    }

}

</script>
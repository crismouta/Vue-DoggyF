<template>
    <router-link
        :to="{
        name: 'MyPostsSitters',
        
        }"
        class="btn text-white m-2 rounded-top rounded-bottom"
        id="buttonMyPostsSitters"
        >MyPostsSitters</router-link>
</template>

<script>
export default {
    name: "ButtonMyPostsSitters",
    
};
</script>

<style scoped>
#buttonMyPostsSitters {
    background: #a15106;
}

</style>
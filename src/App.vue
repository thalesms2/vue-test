<script setup lang="ts">
    import { ref, onMounted } from 'vue'

    const count = ref(0)

    const increment = () => {
        count.value++
    }

    onMounted(() => {
        console.log(`Inicial value is ${count.value}`)
    })
</script>

<template>
    <div>
        Hello World {{count}}
        {{ count > 7 ? 'Gol da alemanha' : 'Ainda não!'}}
        <button @click="increment">Count is {{ count }}</button>
    </div>
</template>

<style scoped>
    div {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    button {
        padding: .5em 1em;
        color: #000020;
        background-color: #fffeee;
        border-radius: .5em;
        margin: .5em;
        border: none;
    }
</style>

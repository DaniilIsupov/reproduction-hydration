<script setup lang="ts">
import { onMounted, ref } from 'vue'
import Child from './components/Child.vue'

const count = ref(0)

onMounted(() => {
    console.log('App.vue')

    count.value += 1
})
</script>

<template>
    <Suspense>
        <Child :count="count" />
    </Suspense>
</template>

<script setup lang="ts">
import { onMounted } from 'vue'

defineProps<{ count: number }>()

onMounted(() => {
    console.log('Child.vue')
})

await new Promise(resolve => setTimeout(resolve, 100))
</script>

<template>
    <div>
        <p
            v-for="(item, index) in Math.pow(2, 8)"
            :key="index"
        >
            Child {{ item }} (count {{ count }})
        </p>
    </div>
</template>

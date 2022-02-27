<template>
    <header>
        <h1>Task tracker Example</h1>
    </header>

    <p>{{ myName }} - {{ version }}</p>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from "@vue/runtime-core"

// using composition API
export default defineComponent({
    setup() {
        const state = reactive({
            myName: 'FlowerPower',
            version: 4 as number | string
        })

        return { ...toRefs(state) }
    }
})
</script>

<style scoped>
header {
    display: flex;
    align-items: center;
    border: 1px dotted rgb(112, 255, 107);
    border-radius: 10px;
    box-shadow: inset;
    height: 100px;
}
</style>
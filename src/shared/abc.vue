<template>
    <div>
        <div class="header">
            <span v-if="open" @click="open=!open">Collapse</span>
            <span v-else="!open" @click="open=!open">Expand</span>

        </div>

        <slot v-if="open">
            <div>Default</div>
        </slot>
    </div>
</template>

<script>
    export default {
        name: 'CollapsibleSection',
        data() {
            return {
                open:true
            }
        }
    }
</script>

<style scoped>
.header {
    background-color: gray;
    padding: 3px;
    cursor: pointer;
}
</style>
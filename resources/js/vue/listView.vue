<template>
    <div>
        <div v-for="(item, index) in items" :key="index" >
            <list-item :item="item" class="item-large" v-on:itemchanged="$emit('reloadlist')" />
        </div>
    </div>
</template>

<script>
import listItem from './listItem';
export default {
    props: ['items'],
    components: {
        listItem
    }
}
</script>

<style scoped>
.item-large{
    background: #e6e6e6;
    padding: 5px;
}
</style>
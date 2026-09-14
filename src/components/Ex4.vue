<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])

// TODO: Add Code Here
const newItem = ref("")

function addItem() {
    items.value.push(newItem.value)
}

function deleteItem(index) {
    items.value.splice(index, 1)
}

</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <li v-for="(item,index) in items">
            {{ item }}
        <button @click="deleteItem(index)">Delete!</button>
        </li>
    </ul>

    <input v-model="newItem" type="text">
    <button @click="addItem">Add!</button>
   
</template>

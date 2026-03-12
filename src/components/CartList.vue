<template>
    <div>
        <cartListItem v-for="cartItem in cartItems"
        :key="cartItem.id"
        :item="cartItem"
        @item-remove="$emit('item-remove', $event)"
        @quantity-update="$emit('quantity-update', $event)"
        ></cartListItem>
    </div>
</template>

<script setup>
import cartListItem from './cartListItem.vue';
defineProps(['cartItems'])
defineEmits(['item-remove', 'quantity-update'])
</script>

<style scoped></style>

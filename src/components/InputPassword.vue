<script setup>
import { ref } from 'vue';

const mostrar = ref(false)
const password = ref('password')
</script>

<template>
    <div class="container text-center input-password">
        <h1 class="my-3">Exercise Input Password</h1>
        <!-- <input type="password" name="" id="password" class="form-control"> -->
        <input :type="mostrar ? 'text' : 'password'" v-model="password" class="form-control" id="password">
        <div class="d-block">
            <span id="show-password" class="mt-2 btn btn-primary" @click="mostrar = !mostrar">Show Password</span>
        </div>
    </div>
</template>

<style lang="css" scoped>
    #show-password:hover {
        cursor: pointer;
        user-select: none;
    }
</style>
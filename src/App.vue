<template>
    <h1>{{ title }}</h1>
    <Modal v-show="modalBool" @close="toggleModal">
        <template v-slot:links>
            <a href="https://www.google.com" target="_blank">google</a>
        </template>
        <h2>HEYYYY</h2>
    </Modal>
    <button @click="toggleModal">Show modal</button>
</template>

<script>
import Modal from "./components/Modal";

export default {
    name: 'App',
    components: {
        Modal
    },
    data() {
        return {
            title: "My first Vue 3 App",
            modalBool: false
        }
    },
    methods: {
        toggleModal() {
            this.modalBool = !this.modalBool;
        }
    }
}
</script>

<style>
    * {
        margin: 0;
        padding: 0;
    }
</style>

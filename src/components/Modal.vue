<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="modal">
            <slot>This is default content</slot>
            <div class="links">
                <slot name="links"></slot>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: [],
        methods: {
            closeModal() {
                this.$emit('close')
            }
        }
    }
</script>

<style scoped>
    .backdrop {
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        background: rgba(0, 0, 0, 0.7);
        position: fixed;
    }

    .modal {
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background: white;
        border-radius: 10px;
    }
</style>
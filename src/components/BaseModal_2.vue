<template>
    <Teleport to="body">
        <Transition name="modal-outer">
            <div v-show="modalActive_2" class="absolute w-full bg-black bg-opacity-50 h-screen top-0 left-0 flex justify-center px-8">
                <Transition name="modal-inner">
                    <div v-if="modalActive_2" class="p-4 bg-white rounded-lg self-start mt-12 max-w-screen-md">
                        <slot />
                        <button class="text-white mt-4 ml-8  bg-blue-700  hover:bg-blue-800 font-medium rounded-lg py-2 px-6" @click="$emit('close-modal_2')">
                            Close
                        </button>
                    </div>
                </Transition>
            </div>
        </Transition>
    </Teleport>
</template>


<script setup>
defineEmits(["close-modal_2"]);
defineProps({
    modalActive_2: {
        type: Boolean,
        default: false,
    }
})
</script>

<style scoped>
    .modal-outer-enter-active,
    .modal-outer-leave-active {
        transition: opacity 0.3s cubic-bezier(0.52, 0.02, 0.19, 1.02)  ;
    }

    .modal-outer-enter-from,
    .modal-outer-leave-to {
        opacity: 0;
    }

    .modal-inner-enter-active {
        transition: all 0.3s cubic-bezier(0.52, 0.02, 0.19, 1.02) 0.15s ;
    }
    .modal-inner-leave-active {
        transition: all 0.3s cubic-bezier(0.52, 0.02, 0.19, 1.02)  ;
    }

    .modal-inner-enter-from {
        opacity: 0;
        transform: scale(0.8);
    }
    .modal-inner-leave-to {
        transform: scale(0.8);
    }

</style>



<template>
  <button @click="setIsOpen(open)">Open Dialog</button>
  <Dialog :open="isOpen" @close="setIsOpen(false)" :initialFocus="initialFocusRef">
    <DialogTitle>Title</DialogTitle>
    <DialogDescription
      >Lorem ipsum, dolor sit amet consectetur adipisicing elit. Distinctio consectetur, vero quo laboriosam eum inventore voluptate optio
      doloribus, odit illo quos itaque harum nulla soluta similique, explicabo rem veniam quis?</DialogDescription
    >
    <button @click="setIsOpen(false)">Cancel</button>
    <button ref="initialFocusRef" @click="setIsOpen(false)">Do it!</button>
  </Dialog>
</template>

<script>
import { ref } from "vue";

import { Dialog, DialogTitle, DialogDescription } from "@headlessui/vue";

export default {
  components: {
    Dialog,
    DialogTitle,
    DialogDescription,
  },
  setup() {
    const isOpen = ref(false);
    const initialFocusRef = ref(null);

    return {
      isOpen,
      initialFocusRef,
      setIsOpen(value) {
        isOpen.value = value;
      },
    };
  },
};
</script>

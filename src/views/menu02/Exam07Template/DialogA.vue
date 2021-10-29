
<!-- component UI definition-->
<template>
    <modal-dialogue-template>
        <template v-slot:header>
            DialogA
        </template>

        <template v-slot:body>
            <p>DialogA 내용입니다.</p>
        </template>

        <template v-slot:footer>
            <button class="btn btn-info btn-sm mr-2" @click="$emit('close')">확인</button>
            <button class="btn btn-info btn-sm mr-2" @click="$emit('close')">닫기</button>
        </template>
    </modal-dialogue-template>
</template>

<script>
import ModalDialogueTemplate from "@/components/menu02/ModalDialogueTemplate.vue";
export default {
    // component's name found in vue devtools on chrome.
    name: "DialogA",
    // component that i want to add
    components: {
        ModalDialogueTemplate
    },
    // component data definition
    data: function() {
        return {
        };
    },
    // component method definition
    methods: {
    }
}
</script>

<!-- component style definition-->
<style scoped>
</style>
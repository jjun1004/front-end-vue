
<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            Exam07Template
        </div>
        <div class="card-body">
            <button class="btn btn-info btn-sm mr-2" @click="modalDialogueTemplate=true">Show ModalDialogueTemplate</button>
            <button class="btn btn-info btn-sm mr-2" @click="dialogA=true">Show DialogA</button>
            <button class="btn btn-info btn-sm mr-2" @click="dialogB=true">Show DialogB</button>
        </div>
        <modal-dialogue-template v-if="modalDialogueTemplate" @close="modalDialogueTemplate=false"/>
        <dialog-a v-if="dialogA" @close="dialogA=false"/>
        <dialog-b v-if="dialogB" @close="dialogB=false"/>
    </div>
</template>

<script>
import ModalDialogueTemplate from "@/components/menu02/ModalDialogueTemplate.vue";
import DialogA from './DialogA.vue';
import DialogB from './DialogB.vue';

export default {
    // component's name found in vue devtools on chrome.
    name: "Exam07Template",
    // component that i want to add
    components: {
        ModalDialogueTemplate,
        DialogA,
        DialogB
    },
    // component data definition
    data: function() {
        return {
            modalDialogueTemplate: false,
            dialogA: false,
            dialogB: false,
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

<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            Exam04View
        </div>
        <div class="card-body">
            <router-view class="mb-2"></router-view>
            <router-view name="rv1" class="mb-2"></router-view>
            <router-view name="rv2" class="mb-2"></router-view>

            <hr/>

            <sub-a-component class="mb-2"/>
            <sub-b-component class="mb-2"/>
            <sub-c-component class="mb-2"/>
        </div>
    </div>
</template>

<script>
import SubAComponent from '@/components/menu01/SubAComponent.vue';
import SubBComponent from '@/components/menu01/SubBComponent.vue';
import SubCComponent from '@/components/menu01/SubCComponent.vue';

export default {
    // component's name found in vue devtools on chrome.
    name: "Exam04View",
    // component that i want to add
    components: {
        SubAComponent,
        SubBComponent,
        SubCComponent
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
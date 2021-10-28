
<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            <span class="title">Exam01View</span>
        </div>
        <div class="card-body">
            <h6>선언적 방식 화면 이동</h6>
            <router-link to="/menu01/exam02view" class="btn btn-info btn-sm mr-2">/menu01/exam02view</router-link>
            <router-link v-bind:to="`/menu01/exam02view`" class="btn btn-info btn-sm mr-2">/menu01/exam02view</router-link>
            <router-link :to="{path:'/menu01/exam02view'}" class="btn btn-info btn-sm mr-2">/menu01/exam02view</router-link>
            <router-link :to="{name: 'menu01_exam02view'}" class="btn btn-info btn-sm mr-2">/menu01/exam02view</router-link>
        </div>
    </div>
</template>

<script>
export default {
    // component's name found in devtools on chrome.
    name: "Exam01View",
    // component that i want to add
    components: {
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
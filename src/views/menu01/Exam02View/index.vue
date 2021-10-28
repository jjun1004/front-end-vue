
<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            <span class="title">Exam02View</span>
        </div>
        <div class="card-body">
            <sub-a-component class="mb-2"/>
            <!-- 프로그램 방식 화면 이동 -->
            <button class="btn btn-info btn-sm mr-2" v-on:click="goUrl">/menu01/exam01view</button>
            <button class="btn btn-info btn-sm mr-2" v-on:click="goUrl()">/menu01/exam01view</button>
            <button class="btn btn-info btn-sm mr-2" @click="goUrl">/menu01/exam01view</button>
            <button class="btn btn-info btn-sm" @click="goUrl()">/menu01/exam01view</button>
        </div>
    </div>
</template>

<script>
import SubAComponent from './SubAComponent';
export default {
    // component's name found in vue devtools on chrome.
    name: "Exam02View",
    // component that i want to add
    components: {
        SubAComponent
    },
    // component data definition
    data: function() {
        return {
        };
    },
    // component method definition
    methods: {
        goUrl: function() {
            this.$router.push("/menu01/exam01view");
            //현재 URL과 동일한 URL로 화면 이동을 할 경우 예외가 발생하므로 예외 처리 코드 필요
            //this.$router.push("/menu01/exam02view").catch(()=>{});

            //this.$router.push({path: "/menu01/exam01view"});
            //this.$router.push({name: "menu01_exam01view"});
        }
    }
}
</script>

<!-- component style definition-->
<style scoped>

</style>
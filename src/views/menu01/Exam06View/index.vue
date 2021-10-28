
<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            Exam06View
        </div>
        <div class="card-body">
            <h6>params(path variable)로 데이터 얻기</h6>
            <div>bno: {{ $route.params.bno }}</div>
            <div>bno: {{ bno }}</div>
        </div>
    </div>
</template>

<script>
export default {
    // component's name found in vue devtools on chrome.
    name: "Exam06View",
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
    },
    //컴포넌트가 생성될 때 실행
    created() {
        console.log("Exam06View 컴포넌트가 생성됨");
        console.log(this.$route);
        console.log(this.$route.params.bno);
    },
    props: [
        "bno"
    ]
}
</script>

<!-- component style definition-->
<style scoped>

</style>
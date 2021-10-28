
<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            Exam08View
        </div>
        <div class="card-body">
            <div>kind: {{$route.query.kind}}</div>
            <div>color: {{$route.query.color}}</div>
            <div>kind: {{kind}}</div>
            <div>color: {{color}}</div>

            <hr/>

            <button class="btn btn-info btn-sm mr-2" @click="goHome">홈으로 이동</button>
            <button class="btn btn-info btn-sm mr-2" @click="goBack">뒤로 이동</button>
        </div>
    </div>
</template>

<script>
export default {
    // component's name found in vue devtools on chrome.
    name: "Exam08View",
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
        goHome() {
            this.$router.push("/");
        },
        goBack() {
            this.$router.go(-1); // 직전으로 이동
        }
    },
    //컴포넌트가 생성된 후 실행되는 메소드
    created() {
        console.log(this.$route);
        console.log(this.$route.query.kind);
        console.log(this.$route.query.color);
    },
    props: [
        "kind",
        "color"
    ]

}
</script>

<!-- component style definition-->
<style scoped>

</style>
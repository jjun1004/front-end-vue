
<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            Exam03View
        </div>
        <div class="card-body">
            <div>
                <h6>선언적 방식 화면(컴포넌트) 전환</h6>
                <router-link to="/menu01/exam03view/subacomponent" class="btn btn-info btn-sm mr-2">SubAComponent</router-link>
                <router-link to="/menu01/exam03view/subbcomponent" class="btn btn-info btn-sm">SubBComponent</router-link>

                <h6 class="mt-2">프로그램 방식 화면(컴포넌트) 전환</h6>
                <button @click="goUrl('a')" class="btn btn-info btn-sm mr-2">SubAComponent</button>
                <button @click="goUrl('b')" class="btn btn-info btn-sm mr-2">SubBComponent</button>
            </div>

            <div class="mt-2">
                <router-view></router-view>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    // component's name found in vue devtools on chrome.
    name: "Exam03View",
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
        goUrl(kind) {
            this.$router.push(`/menu01/exam03view/sub${kind}component`)
            .catch(()=> {});
        }
    }
}
</script>

<!-- component style definition-->
<style scoped>

</style>
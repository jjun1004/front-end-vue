
<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            Exam01Props
        </div>
        <div class="card-body">
            <child-a :prop1="data1" 
                    :prop2="data2"
                    :productNo="pno"
                    :product-kind="pkind"
                    :product-price="pprice"/>
        </div>
    </div>
</template>

<script>
import ChildA from "./ChildA.vue";

export default {
    // component's name found in vue devtools on chrome.
    name: "Exam01Props",
    // component that i want to add
    components: {
        ChildA
    },
    // component data definition
    data: function() {
        return {
            data1: "value1",
            data2: "value2",
            pno: "1",
            pkind: "bag",
            pprice: 1000
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

<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            Exam01Expressions
        </div>
        <div class="card-body">
            <h5>상품정보</h5>
            <p>번호: {{no}}</p>
            <p>이름: {{name}}</p>
            <p>회사: {{company}}</p>
            <p>가격: {{getPrice()}}</p>
            <p>판매여부: {{sale?"판매":"품절"}}</p>
            <button class="btn btn-info btn-sm mt-2" @click="changeData">변경</button>
        </div>
    </div>
</template>

<script>
export default {
    // component's name found in vue devtools on chrome.
    name: "Exam01Expressions",
    // component that i want to add
    components: {
    },
    // component data definition
    data: function() {
        return {
            no: 1,
            name: "미니백",
            company: "클레인",
            price: 300000,
            sale: true
        };
    },
    // component method definition
    methods: {
        getPrice() {
            return this.price;
        },
        changeData() {
            this.price+=1000;
            this.sale = !this.sale;
        }
    }
}
</script>

<!-- component style definition-->
<style scoped>

</style>
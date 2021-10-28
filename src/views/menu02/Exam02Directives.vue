
<!-- component UI definition-->
<template>
    <div class="card">
        <div class="card-header">
            Exam02Directives
        </div>
        <div class="card-body">
            <div>
                <img class="mr-2" src="@/assets/photos/photo1.jpg" height="100px"/>
                <img v-bind:src="require(`@/assets/photos/${photoFileName}`)" height="100px"/>
            </div>
            <hr/>
            <button class="btn btn-info btn-sm" @click="changeData">변경</button>
        </div>
    </div>
</template>

<script>
export default {
    // component's name found in vue devtools on chrome.
    name: "Exam02Directives",
    // component that i want to add
    components: {
    },
    // component data definition
    data: function() {
        return {
            photoFileName: "photo2.jpg"
        };
    },
    // component method definition
    methods: {
        changeData() {
            if(this.photoFileName === "photo2.jpg"){
                this.photoFileName = "photo3.jpg";
            } else {
                this.photoFileName = "photo2.jpg";
            }
        }
    }
}
</script>

<!-- component style definition-->
<style scoped>

</style>
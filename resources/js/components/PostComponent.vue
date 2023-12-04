<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Post Component</div>
                    <div class="card-body">
                        I'm an post component.
                        <div>Имя: {{name}}</div>
                        <button @click="sayHello">Hello</button>
                    </div>

                    <SinglePostComponent></SinglePostComponent>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import SinglePostComponent from "@/components/SinglePostComponent.vue";

export default {
    name: "PostComponent",
    data() {
        return {
            name: "Vasya",
        }
    },
    methods: {
        sayHello() {
            alert(this.name);
        },
    },
    components: {SinglePostComponent}
}
</script>

<style scoped>

</style>

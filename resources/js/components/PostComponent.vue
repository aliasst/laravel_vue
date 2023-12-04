<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Post Component</div>
                    <div class="card-body">
                        <table class="table">
                            <thead>
                            <tr>
                                <th scope="col">#</th>
                                <th scope="col">Name</th>
                                <th scope="col">Age</th>
                                <th scope="col">Job</th>
                            </tr>
                            </thead>
                            <tbody>
                            <tr v-for="person in personsMore" >
                                <th scope="row">{{person.id}}</th>
                                <td>{{person.name}}</td>
                                <td>{{person.age}}</td>
                                <td>{{person.job}}</td>
                            </tr>

                            </tbody>
                        </table>

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
            persons: [
                {
                    id: 1,
                    name: "Vasya",
                    age: 20,
                    job: "coach"
                },
                {
                    id: 2,
                    name: "Misha",
                    age: 39,
                    job: "proger"
                },
                {
                    id: 3,
                    name: "Oleg",
                    age: 40,
                    job: "rab"
                },
                {
                    id: 4,
                    name: "Timon",
                    age: 20,
                    job: "secret"
                },
                {
                    id: 5,
                    name: "Ivan",
                    age: 50,
                    job: "driver"
                },

            ]
        }
    },
    methods: {
        sayHello() {
            //alert(this.name);
            alert(this.test)
        },
    },
    computed: {
        test() {
            return this.name + ' работает в рюмочной';
        },
        personsMore(){
            return this.persons.filter(function (person){
                return person.age > 20;
            });
        }
    },

    components: {SinglePostComponent}
}
</script>

<style scoped>

</style>

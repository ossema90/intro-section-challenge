<template>
    <div class="d-flex align-center ">
        <div class="ml-16 pa-2 mt-4">
            <img :src="logo" />
        </div>
        <div class="d-flex align-center mx-16">

            <div>
                <button class="justify-center pa-4">
                    Features <v-icon start icon="mdi-menu-down"></v-icon>
                    <v-menu activator="parent" flat>
                        <v-list>
                            <v-list-item v-for="(feature, index) in features" :key="index" class="">
                                <div class="d-flex">
                                    <img :src="feature.img" class="ma-2" />
                                    <v-list-item-title class="ma-2">
                                        {{ feature.title }}</v-list-item-title>
                                </div>
                            </v-list-item>
                        </v-list>
                    </v-menu>
                </button>
            </div>
            <div>
                <button class="justify-center pa-4">
                    Company <v-icon start icon="mdi-menu-down"></v-icon>
                    <v-menu activator="parent" flat>
                        <v-list>
                            <v-list-item v-for="(company, index) in companies" :key="index" class="justify-left ml-2">
                                <v-list-item-title> {{ company.title }}</v-list-item-title>
                            </v-list-item>
                        </v-list>
                    </v-menu>
                </button>
            </div>
            <div class="mx-8">Careers</div>
            <div class="mx-8">About</div>
        </div>
        <v-spacer></v-spacer>
        <div class="d-flex align-center " style="margin-left: auto;">

            <div class="mx-4">
                <button style="width: 10rem;">Login</button>
            </div>
            <div class="mx-4">
                <button class="" style="border: solid 3px; border-radius: 0.5rem; padding: 0.5rem 0.5rem ; width:10rem ;">
                    Register
                </button>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            logo: require("../assets/logo.svg"),
            calendarIcon: require("../assets/icon-calendar.svg"),
            features: [
                {
                    title: "Todo List",
                    img: require("../assets/icon-todo.svg"),
                },
                {
                    title: "Calendar",
                    img: require("../assets/icon-calendar.svg"),
                },
                {
                    title: "Reminders",
                    img: require("../assets/icon-reminders.svg"),
                },
                {
                    title: "Planning",
                    img: require("../assets/icon-planning.svg"),
                },
            ],
            companies: [
                {
                    title: "History",
                },
                {
                    title: "Our Team",
                },
                {
                    title: "Blog",
                },
            ],
        };
    },
};
</script>

<style></style>

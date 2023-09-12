<template>
    <div>
        <h1 v-if="showTitle" >{{ message }}</h1>
        <p v-else >Title is not visible</p>
        <p>{{ description }}</p>
    <form>
        <input v-model="userInput"/>
        <p>User input: {{ userInput }}</p>
    </form>
    <ul>
        <li v-for="(item, index) in arrayOfItems" :key="index">{{ item }}</li>
    </ul>
    
    </div>
</template>

<script>

export default {
    data() {
        return {
            showTitle: false,
            message: "Hello, this is my component",
            description: "I think I'am a very good developer",
            userInput: "",
            arrayOfItems: ["Book", "Ball", "Laptop", "Hat"]
        }
    }
}
</script>

<style>
h1 {
    color: aqua;
}
</style>
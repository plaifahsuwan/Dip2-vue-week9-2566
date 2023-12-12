<template>
    <div>
        <!-- <h1>{{ name }}</h1>
        <p>{{ task[0] }} </p>
        <p>{{ task[1] }}</p>
        <hr> -->
        <!-- <ComponentA />
        <ComponentB />
        <ComponentC /> -->
        <!-- <hr /> -->
        <p>{{ firstName }} {{ lastName }}</p>
        <p>{{ fullName }}</p>
    </div>
</template>

<script>
// import ComponentA from './ComponentA.vue';
// import ComponentB from './ComponentB.vue';
// import ComponentC from './ComponentC.vue';
export default {
    name: 'GreetingMessage',
    // props:['firstName', 'lastName', 'fullName'],
    props: {
        firstName: String,
        lastName: String,
        fullName: {
            type: String,
            required: false
            // default:'Unknow'
        }
    },
    components: {
        // ComponentA,
        // ComponentB,
        // ComponentC,
    },
    data() {
        return {
            name: 'Mark Zuckerberg',
            task: [
                { id: 1, title: 'buy some milk', isFave: false },
                { id: 2, title: 'play game', isFave: true },
            ]
        }
    },
}
</script>
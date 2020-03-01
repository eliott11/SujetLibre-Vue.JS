<template>
    <div>
        <ul id="v-for-object">
        <li v-for="title in object"
            {{ title }}. {{ author }}: {{ date }}: {{ text }}
        </li>
        </ul>
        <v-row justify="space-around">
            <v-avatar>
                <img src="https://cdn4.iconfinder.com/data/icons/superheroes/512/ironman-512.png" alt="John">
            </v-avatar>
        </v-row><br><br>
    </div>
</template>

<script>
    export default {
        el: '#v-for-object',
        data () {
            return {
                items: {
                    title: 'How to do lists in Vue',
                    author: 'Jane Doe',
                    date: '2016-04-10',
                    text: 'Hello'
                },
            }
        },
    }
</script>
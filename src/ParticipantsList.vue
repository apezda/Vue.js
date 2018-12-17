<template>
    <div><div>
        <h1 v-if="list.length > 0" > Participants list </h1>
        <ol>
            <li v-for="person in list"> {{person}}</li>
        </ol>
    </div>


    </div>
</template>

<script>
    export default {

            props: ['list']

    }

</script>
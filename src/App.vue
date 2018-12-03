<template>
  <div>
    <h1> Clicked {{ times }} times. </h1>
    <button @click="Increase()">More!</button>
    <button @click="Start()"> Start over! </button>
  </div>
</template>

<script>
    export default {
        data() {
            return {times: 0}
        },
        methods: {
            Increase() {
                this.times += 1;
            },
            Start () {
                this.times = 0;
            }
        }
    };
</script>

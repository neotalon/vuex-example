Vue.component('counter', {
props: ['timeLeft'],

<template>
          <div>
              {{ count }}
          </div>
</template>
})
<script>
    export default {
        name: "AttackButton",
        props: {
            timeLeft: String,
            minutesLeft: Number
        },
        methods: {
            makeZero() {
                this.timeLeft = "0";
            },
            getTime() {
                let num = this.minutesLeft;
                let hours = (num / 60);
                let rhours = Math.floor(hours);
                let minutes = (hours - rhours) * 60;
                let rminutes = Math.round(minutes);
                return rhours + ":" + rminutes;
            }
        }
    }
</script>

<style scoped>
    {
        text-transform: none !important;
    }
</style>
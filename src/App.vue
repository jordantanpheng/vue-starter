<template>
  <div>  
    <h1>{{ "Clicked " + count + " times" }}</h1>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>
 
<script>
    export default {
        data() {
            return {count : 0}
        },
        methods: {
            iAmClicked() {
				this.count += 1;
            }
        }
    };
</script>
<template>
  <div>  
    <h1>{{ title }}</h1>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>
 
<script>
	var count = 0;
    export default {
        data() {
            return {title: 'Clicked 0 times'}
        },
        methods: {
            iAmClicked() {
				count++;
                this.title = 'Clicked ' + count + ' times';
            }
        }
    };
</script>
<template>
  <div>
    <form @submit.prevent="add()">
	<div class="form-group">
      <label>Conversion unit</label>
      <input type="text" class="form-control" placeholder="Enter conversion unit" v-model="newUnit.conversion unit">
      <label>Base multiplier</label>
      <input type="text" class="form-control" placeholder="Enter base multiplier" v-model="newUnit.base multiplier">
	  <br>
      <button class="btn btn-primary mb-2">Add</button>
	</div>
    </form>
  </div>
</template>

<script>
  export default {
    data() {
      return {newUnit: {}};
    },
    methods: {
      add() {
        this.$emit('added', this.newUnit);
        this.newUnit = {};
      }
    }
  };
</script>
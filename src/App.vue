<template>
  <div>
    <div>
	  <h1>Unit Converter</h1>
	  <units-list :list="units" @removed="removeUnit($event)"></units-list>
    </div>
    <h3>Add new conversion unit</h3>
    <new-unit-form @added="addnewUnit($event)"></new-unit-form>
  </div>
</template>

<script>
  import ValuesList from "./ValuesList.vue";
  import UnitsList from "./UnitsList.vue";
  import NewConversionUnit from "./NewConversionUnit.vue";
  export default {
    components: {NewConversionUnit, UnitsList},
    data() {
      return {
	    units: []
	  };
    },
    methods: {
      addnewUnit(newUnit) {
        this.units.push(newUnit);
      },
	  removeUnit(unit) {
	    this.units.remove(unit);
	  }
    }
  };
</script>
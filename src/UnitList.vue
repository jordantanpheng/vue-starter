 <template>
  <div>
    <ol>
        <li v-for="person in list" :key="person">
            {{ person.firstname }} {{ person.lastname }}
        </li>
    </ol>
  </div>
</template>

<script>
  export default {
    props: ['list'],
    methods: {
      remove() {
        this.$emit('removed', i);
      }
	}
  };
</script>
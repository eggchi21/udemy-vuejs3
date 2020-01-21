<template>
  <div>
    <h3>Homes</h3>
    <button @click="toUsers">Usersへいく</button>
    <p>{{ count }}</p>
  </div>
</template>

<script>
export default {
  computed: {
    count(){
      return this.$store.state.count;
    }
  },
  methods: {
    toUsers(){
      this.$router.push({
        name:'user-id-profile',
        params:{id: 1}
      });
    }
  }
}
</script>
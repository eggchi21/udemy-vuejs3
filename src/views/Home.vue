<template>
  <div>
    <h3>Homes</h3>
    <button @click="toUsers">Usersへいく</button>
  </div>
</template>

<script>
export default {
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
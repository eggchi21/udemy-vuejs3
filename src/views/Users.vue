<template>
  <div>
    <h3>Users</h3>
    <router-link to="/users/1">user1</router-link>
    <router-link to="/users/2">user2</router-link>

    <hr>
    <h1>User No.{{id}}</h1>
    <router-link :to="'/users/' + (Number(id) + 1) + '/profile?lang=ja' ">next user</router-link>
    <router-link :to="{name:'user-id-profile',params:{id:Number(id) + 1},query:{lang:'ja',page:2}}">next user</router-link>
    <router-view></router-view>
    <div style="height: 700px;"></div>
    <router-link
    id="next-user"
    :to="{name:'user-id-profile',params:{id:Number(id) + 1},query:{lang:'ja',page:2},hash: '#next-user'}">next user</router-link>

  </div>
</template>

<script>
export default {
  props:["id"]
}
</script>
<template>
  <div>
    <ul>
      <li class="active">HOME</li>
       <li v-for="list in lists" :key="list">{{list.toUpperCase()}}</li>
    </ul>

  </div>
</template>

<script>
export default {
  props: {
    lists: Array
  }
}
</script>

<style lang="scss">
ul {
  display: flex;
  list-style: none;
  li {
    padding: 0 1rem;
    font-size: 0.5rem;
    color: #74559F;
  }
  .active {
      color: #74559F;
      &::after {
        content: "";
        display: block;
        width: 30px;
        height: 2px;
        background-color: #74559F;
        margin: auto;
        margin-top: 5px;
      }
    }
}
</style>

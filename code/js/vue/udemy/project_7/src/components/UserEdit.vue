<template>
    <div class="component">
        <h3>You may edit the User here</h3>
        <p>Edit me!</p>
        <p>My age {{ userAge }}</p>
        <button @click='editAge' name="button">Age me</button>
    </div>
</template>

<script>

  import { eventBus } from '../main';

  export default {
    props: ['userAge'],
    methods: {
      editAge () {
        this.userAge = 40;
        eventBus.changeAge(this.userAge);
      }
    }
  }
</script>

<style scoped>
    div {
        background-color: lightgreen;
    }
</style>

<script lang="ts">
import { defineComponent } from '@vue/runtime-core';

// let age: number | string = 0; // <- type union

export default defineComponent({
  name: 'App',
  components: {},
  data() {
    return {
      name: 'Link',
      age: 17 as number | string, // <- type assertion
    };
  },
  methods: {
    changePerson(name: string, age: number | string) {
      this.name = name;
      this.age = age;
      return name, age; // side effect with comma operator
    },
  },
});
</script>

<template>
  <h1>Hello, {{ name }}</h1>
  <h2>Age: {{ age }}</h2>
  <button @click="changePerson('Zelda', 16)">Change name</button>
</template>

<style></style>

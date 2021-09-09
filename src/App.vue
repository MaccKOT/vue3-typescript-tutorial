<template>
  <!-- 
  <h1>Hello, {{ name.value }}</h1>
  <h2>Age: {{ age.value }}</h2>
  <button @click="changePerson('Zelda', 16)">Change name</button>
  -->

  <div class="app">
    <p>{{ jobs[0].location }}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from '@vue/runtime-core';
import Job from '@/types/Job';

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    // composition API

    // const state = reactive({
    //   name: 'Link',
    //   age: 17 as number | string,
    // });

    // return {
    //   ...toRefs(state),
    // };

    // Ref's style
    // const name = ref('Link');
    // const age = ref<number | string>(17);

    // return { name, age };

    const jobs = ref<Job[]>([
      {
        title: 'farm worker',
        location: 'lon lon ranch',
        salary: 30000,
        id: '1',
      },
      {
        title: 'quarryman',
        location: 'death mountain',
        salary: 40000,
        id: '2',
      },
      {
        title: 'flute player',
        location: 'the lost woods',
        salary: 35000,
        id: '3',
      },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      {
        title: 'prison guard',
        location: 'gerudo valley',
        salary: 32000,
        id: '5',
      },
    ]);

    return { jobs };
  },
  methods: {
    //   changePerson(name: string, age: number | string) {
    //     this.name = name;
    //     this.age = age;
    //     return { name, age };
    //   },
  },
});
</script>

<style></style>

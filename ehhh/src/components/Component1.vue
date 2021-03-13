<template>
  <div>
    <h1>{{ startsWithLetter ? componentName.toUpperCase() : 'Starts with number' }}</h1>
  </div>
</template>

<script>

export default {
  name: 'Component1',
  data() {
    return {
      componentName: 'Component1',
      startsWithLetter: false,
    };
  },
  methods: {
    changeComponentName(name) {
      this.componentName = name;
    },
  },
};

</script>

<style>
h1 {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

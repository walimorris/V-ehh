<template>
  <div>
    <h1>{{ title }}</h1>
    <h2>{{ subtitle }}</h2>
    <ul class="list_one">
      <li>{{ items[0] }}</li>
      <li>{{ items[1] }}</li>
      <li>{{ items[2] }}</li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'Component2',
  data() {
    return {
      title: 'Component2',
      subtitle: 'Vue JS Basics',
      items: ['item1', 'item2', 'item3'],
    };
  },
  methods: {},
};

</script>

<style>
h1 {
  margin-top: 60px;
  text-align: center;
  color: #2c3e50;
}

h2 {
  margin-top: 60px;
  text-align: center;
  color: #4fc08d;
}

.list_one {
  display: block;
  margin: 0 auto;
  max-width: 400px;
  padding: 30px;
  border: 10px solid rgba(0,0,0,0.25);
}

li {
  color: #2c3e50;
  margin-bottom: 4px;
}

</style>

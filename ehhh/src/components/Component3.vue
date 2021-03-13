<template>
  <div>
    <h1 v-show="true" v-once v-text="text">Loading...</h1>
    <h2 v-html="html"/>
    <a :href="link.url" v-text="link.title"/>
  </div>
</template>

<script>
export default {
  name: 'Component3',
  data() {
    return {
      text: 'Directive text',
      html: 'Stylise</br>HTML in<br/>your data</b>',
      link: {
        url: 'https://www.google.com',
        title: 'Go to Google',
      },
    };
  },
};

</script>

<style>
h1 {
  margin: 40px 0 0;
  font-weight: normal;
}

</style>

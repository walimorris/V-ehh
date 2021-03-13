<template>
  <div class="message">
    <button v-on:click="changeMessageOnClick()" class="message_button">
      {{ message }}
    </button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      messages: ['hello', 'hello-there', 'oh-rah!', 'Semper-fi'],
      messageIndex: 0,
      message: 'click-me',
    };
  },
  methods: {
    changeMessageOnClick() {
      if (this.messageIndex === this.messages.length - 1) {
        this.messageIndex = 0;
      } else {
        this.messageIndex += 1;
      }
      this.message = this.messages[this.messageIndex];
    },
  },
};

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.message {
  text-align: center;
  color: bisque;
}

.message_button {
  text-align: center;
  color: black;
  font-size: 35px;
}

</style>

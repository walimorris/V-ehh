<template>
  <div v-show="isShowClickModal">{{ text }}
    <button v-on:click="unShowClickModalMessage()">Click Me</button>
  </div>
</template>

<script>
import Cookies from 'js-cookie';

export default {
  name: 'ClickModal',
  data() {
    return {
      isShowClickModal: true,
      text: 'You will see this only if the - click_undone_token - is not present.',
      isCookiePresent: false,
    };
  },
  created() {
    /**
     * Checks if click_undone_token is present. If cookie is present: the un-doable
     * button will not render. If cookie is not present: un-doable button will render.
     */
    const clickCookie = Cookies.get('click_undone_token');
    if (clickCookie === undefined) {
      this.showClickModalMessage();
    } else {
      this.unShowClickModalMessage();
    }
    console.log(document.cookie);
  },
  methods: {
    /**
     * Handles the render of the un-doable button.
     */
    showClickModalMessage() {
      this.isShowClickModal = true;
    },
    /**
     * Handles the un-doable button not being rendered. In this case, the
     * click-undone_token is present so the un-doable button is not rendered.
     * A cookie is created, if it doesn't exit.
     */
    unShowClickModalMessage() {
      this.isShowClickModal = false;
      this.createClickCookie();
    },
    /**
     * Handles creating the click_undone_token cookie, if it doesn't exist.
     */
    createClickCookie() {
      if (this.isCookiePresent === false) {
        Cookies.set('click_undone_token', 'anonymous', { expires: 7 }, { secure: true });
      }
      this.isCookiePresent = true;
    },
  },
};

</script>

<style>

</style>

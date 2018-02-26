<template>
  <div>
    <message :msg="msg"></message>
    <button id="toggle-message" @click="toggleMessage">
      Change message
    </button>
    <img :src="image" />
  </div>
</template>

<script>
import Message from './Message'
import logo1 from '@/assets/logo1.png'
import logo2 from '@/assets/logo2.png'

export default {
  name: 'message-toggle',
  data: () => ({
    msg: null,
    image: logo1
  }),
  methods: {
    toggleMessage () {
      this.image = this.image === logo1 ? logo2 : logo1
      this.msg = this.msg === 'message' ? 'toggled message' : 'message'
    }
  },
  components: {
    Message
  }
}
</script>

<template>
  <div class="container">
    <p>
        madafaka
    </p>
  </div>
</template>

<script lang="ts">
import Vue, { PropOptions } from 'vue'
// import { Vue, Component, Prop } from 'vue-property-decorator'
import Logo from '~/components/Logo.vue'
import User from '~/components/User.vue'
import User2 from '~/components/User2.vue'

interface User {
  firstName: string
  lastName: string
}

export default Vue.extend({
  components: {
    Logo,
    User,
    User2,
  },

  data() {
    const user: User = {
      firstName: 'John',
      lastName: 'Doe',
    }

    return {
      count: 0,
      message: 'This is a message',
      user,
    }
  },

  computed: {
    fullName(): string {
      return `${this.user.firstName} ${this.user.lastName}`
    },
  },

  methods: {
    async increment() {
      this.count++
    },

    decrement() {
      this.count--
    },
  },
})
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.my-5 {
  margin: 20px 0;
}
</style>

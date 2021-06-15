<template>
  <div>
    <v-btn
      @click="googleLogin"
    >
      login
    </v-btn>
    <div>v-if logout</div>
  </div>
</template>

<script lang="ts">
  export default {
    methods: {
      googleLogin () {
        this.$store.dispatch('googleLogin')
      },
    }
  }
</script>

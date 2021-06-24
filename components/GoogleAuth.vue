<template>
  <div>
    <v-btn
      @click="googleLogin"
    >
      login
    </v-btn>
    <div>logout</div>
  </div>
</template>

<script lang="ts">
  import { defineComponent, useContext } from '@nuxtjs/composition-api'

  export default defineComponent({
    setup() {
      const { $fire, $fireModule } = useContext()
      const googleLogin = async () => {
        try {
          const provider = new $fireModule.auth.GoogleAuthProvider()
          $fire.auth.signInWithRedirect(provider)
        } catch (e) {
          console.error(e)
        }
      }

      return { googleLogin }
    }
  })
</script>

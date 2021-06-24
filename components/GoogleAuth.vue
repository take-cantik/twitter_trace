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
  import { define } from '@nuxtjs/composition-api'

  export default defineComponent({
    setup(_, { root }) {
      const googleLogin = async () => {
        try {
          const provider = new root.$fireModules.auth.GoogleAuthProvider()
          root.$fire.auth.signInWithRedirect(provider)
        } catch (e) {
          console.error(e)
        }
      }

      return { googleLogin }
    }
  })
</script>

<template>
  <header>
    <NuxtLink to="/">Home</NuxtLink>
    <NuxtLink to="/mypage">MyPage</NuxtLink>
    <google-auth />
  </header>
</template>

<script>
  import GoogleAuth from '~/components/GoogleAuth.vue'

  export default {
    components: {
      GoogleAuth,
    }
  }

</script>

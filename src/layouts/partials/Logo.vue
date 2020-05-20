<template>
  <div class="logo" @contextmenu="rightClick" oncontextmenu="return false;">
    <g-link class="logo__link" to="/" title="Back to home">
      <Logo class="logo__svg hide-for-small" alt="PMI Kabupaten Kudus" />
      <LogoSmall class="logo__svg show-for-small logo__svg--small" alt="PMI Kabupaten Kudus" />
    </g-link>
  </div>
</template>

<script>
import Logo from '~/assets/images/pmikudus-logo.svg'
import LogoSmall from '~/assets/images/pmikudus-logo-small.svg'
export default {
  components: {
    Logo,
    LogoSmall
  },
  methods: {
    rightClick() {
      return false
    }
  }
}
</script>

<style lang="scss">
 .logo {
  &__svg{
  	max-width: 130px;
  	height: auto;
    margin-top: -3px;
    &--small {
      max-width: 25px;
    }
  }
 }
</style>

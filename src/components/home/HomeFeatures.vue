<template>
  <Section dots="true">
    <div class="container text-center container-sm mb">
      <h2>7 Prinsip Dasar Palang Merah dan Bulan Sabit Merah Internasional</h2>
    </div>
    <div class="homepage-features grid-cols">

      <Feature>
        <h3>Kemanusiaan</h3>
      </Feature>

      <Feature>
        <h3>Kesamaan</h3>
      </Feature>

      <Feature>
        <h3>Kenetralan</h3>
      </Feature>

      <Feature>
        <h3>Kemandirian</h3>
      </Feature>

      <Feature>
        <h3>Kesukarelaan</h3>
      </Feature>

      <Feature>
        <h3>Kesatuan</h3>
      </Feature>

      <Feature>
        <h3>Kesemestaan</h3>
      </Feature>

    </div>

  </Section>
</template>

<script>
import VueLogo from '~/assets/images/vue-logo.svg'
import GraphQlLogo from '~/assets/images/graphql-logo.svg'
export default {
  props: ['icon'],
  components: {
    VueLogo,
    GraphQlLogo,
  },
  computed: {
    iconClasses() {
      let classes = []
      return classes
    }
  }
}
</script>

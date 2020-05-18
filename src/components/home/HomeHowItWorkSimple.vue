<template>
  <Section class="works">
    <div class="grid-cols grid-cols--gap-large grid-cols--full-md">

      <Card title="Pintasan">
        <ul class="bullet-list mb">
          <li><Bullet /><g-link to="/stokdarah/">Stok Darah PMI Kudus</g-link></li>
          <li><Bullet /><g-link to="/berita/">Berita PMI kudus</g-link></li>
          <li><Bullet /><g-link to="/kontak/">Kontak</g-link></li>
          <li><Bullet /><g-link to="/laman/">Laman</g-link></li>
        </ul>

        <template slot="outer">
          <Dots class="hide-for-small"/>
          <Dots class="dots--vertical show-for-small"/>
        </template>
      </Card>

      <Card title="Sambutan" class="text-center flex-align-middle">

        <div class="works__logo">
          <sambutan />
          <div class="works__pulse-bg"></div>
          <div class="works__pulse-bg"></div>
        </div>

        <p class="works__tools flex gap-15 text-center flex--center">
          <g-link to="/sambutan/">Sambutan Kepala<br/><strong>PMI Kabupaten Kudus</strong></g-link>
        </p>

        <template slot="outer">
          <Dots class="hide-for-small"/>
          <Dots class="dots--vertical show-for-small"/>
        </template>
      </Card>

      <Card title="Website Terkait">
        <ul class="bullet-list mb">
          <li><Bullet /><a href="//pmi.or.id/" rel="noopener" target="_blank">PMI Pusat</a></li>
          <li><Bullet /><a href="//pmi-jateng.or.id/" rel="noopener" target="_blank">PMI Jawa Tengah</a></li>
          <li><Bullet /><a href="//kuduskab.go.id/" rel="noopener" target="_blank">Pemkab Kudus</a></li>
        </ul>
      </Card>

    </div>
  </Section>
</template>

<script>
import GraphQlLogo from '~/assets/images/graphql-logo.svg'
import VueLogo from '~/assets/images/vue-logo.svg'
import WebpackLogo from '~/assets/images/webpack-logo.svg'
import Sambutan from '~/assets/images/sambutan.svg'
import Bullet from '~/assets/images/bullet.svg'
import Dots from '~/components/Dots.vue'

export default {
  components: {
    Bullet,
    VueLogo,
    Sambutan,
    WebpackLogo,
    GraphQlLogo,
    Dots
  }
}
</script>

<style lang="scss">
.works {

  .bullet-list li {
    margin-bottom: .3rem;
  }

  .card__inner {
    padding: 30px 40px;
  }

  @media screen and (max-width: 850px) {
    .card {
      margin-bottom: 40px;
    }
  }


  &__tools {
    border: 1px solid var(--border-color);
    max-width: 230px;
    border-radius: 4px;
    z-index: 9;
    margin: 0 auto!important;
    padding: 10px;

    li {
      margin-bottom: 0;
    }
  }

  &__logo {
    background-color: var(--primary-color-dark);
    width: 100px;
    z-index: 1;
    position: relative;
    height: 100px;
    margin: 0 auto;
    margin-top: 18%;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    border-radius: 100%;
    z-index: 0;
    margin-bottom: 1rem;
    animation: bounce 2s infinite;

    svg {
      width: 70px;
      height: 70px;
    }
  }

  &__pulse-bg {
    animation: pulse 2s infinite;
    border: 3px solid var(--primary-color);
    width: 100px;
    height: 100px;
    position: absolute;
    border-radius: 100%;
    opacity: .3;
    z-index: -1;

    + .works__pulse-bg {
      width: 95px;
      height: 95px;
      animation-delay: .3s;
    }
  }

  &__powered-by {
    opacity: .8;
    line-height: 1.3;
    padding-bottom: 1.2rem;
  }
}
</style>

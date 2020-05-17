<template>
  <Section class="intro" dots="true">
    <div class="container text-center ">

        <div class="intro__message mb" hidden></div>

        <h1 class="intro__title">
          <span>PMI Kabupaten Kudus</span>
        </h1>

        <p class="intro__lead lead post mb">
          Jl. Kudus - Purwodadi (Depan RS Mardi Rahayu), Jati Kulon Kudus <g-link to="https://goo.gl/maps/f4WCXbhj2UEyShVt6">(Buka Google Maps)</g-link> 🚀
        </p>

        <p class="intro__links">
          <g-link  to="/kontak/" class="button primary button--large">
            <span>Hubungi Kami</span>
          </g-link>
        </p>

        <p class="intro__info">
          <span>Open-source MIT Licensed. </span>
          <a href="//github.com/gridsome/gridsome" target="_blank" rel="noopener noreferrer">
            <span>GitHub (v{{ $static.metadata.gridsomeVersion }})</span>
          </a>
        </p>
    </div>
  </Section>
</template>

<static-query>
query {
  metadata {
    gridsomeVersion
  }
}
</static-query>

<script>
export default {
  data () {
    return {
      currentText: 0
    }
  },
  mounted () {
    (($vm) => {
      (function animate () {
        $vm._counter = setTimeout(() => {
          $vm.currentText = ($vm.currentText + 1) % 6
          requestAnimationFrame(animate)
        }, 1500)
      })()
    })(this)
  },
  destroyed () {
    clearTimeout(this._counter)
  },
}
</script>

<style lang="scss">

.intro {
  padding: calc(2% + var(--space)) 0;

  &__title {
    font-size: 3rem;
    font-weight: 600;
    margin-left: auto;
    margin-right: auto;

    @media screen and (max-width: 850px) {
      & {
        font-size: 2rem;
      }
    }
  }

  &__lead {
    max-width: 650px;
    margin-left: auto;
    margin-right: auto;
    font-size: 1.3rem;

    @media screen and (max-width: 850px) {
      & {
        font-size: 1rem;
      }
    }
  }

  &__info {
    font-size: .9rem;
  }

  &__keywords {
    position: relative;
    display: block;
  }
}
</style>

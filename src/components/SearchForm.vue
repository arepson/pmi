<template>
  <form
    :id="id"
    class="header-search"
  >
    <label>
    </label>
  </form>
</template>

<script>
export default {
  props: {
    id: { type: String, default: 'search' }
  },

  data () {
    return {
      isLoaded: false
    }
  },

  methods: {
    onFocus () {
      if (this.isLoaded) return

      import('docsearch.js').then(({ default: docsearch }) => {
        docsearch({
          indexName: 'PMI',
          inputSelector: `#${this.id}-input`,
          apiKey: '4d68a7d548c5ffc61a92dba71fb6893c',
          debug: process.env.NODE_ENV === 'development'
        })

        this.isLoaded = true

        this.$nextTick(() => this.$refs.input.focus())
      })
    }
  }
}
</script>

<style lang="scss">
@import '~docsearch.js/dist/cdn/docsearch.min.css';

.header-search {
  display: block;
  margin-bottom: 0;
  font-size: 0.9rem;
  flex: 1;
  width: 100%;

  label {
    display: flex;
    align-items: center;
  }

  .search-icon {
    margin-left: -1.66rem;
    width: 1rem;
    pointer-events: none;
    opacity: .6;
  }

  @media screen and (max-width: 550px) {
    & { margin: 0 3px 0 -15px; }

    .algolia-autocomplete .ds-dropdown-menu {
      position: fixed!important;
      left:0!important;
      top: var(--header-height)!important;
      right:50px!important;
      &:before {
        display: none!important;
      }
    }
  }

  .algolia-autocomplete {
    width: 100%;
  }
}

.algolia-autocomplete .algolia-docsearch-suggestion--wrapper {
  padding-top: 0;
}
</style>

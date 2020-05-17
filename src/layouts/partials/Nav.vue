<template>
  <nav class="main-nav flex gap-15">
    <g-link to="/berita/">
      <span class="main-nav__label">Berita</span>
    </g-link>

    <g-link to="/laman/">
      <span class="main-nav__label">Laman</span>
    </g-link>

    <g-link to="/kontak/">
      <span class="main-nav__label">Kontak</span>
    </g-link>

    <g-link to="/stokdarah/">
      <span class="main-nav__label">Stok Darah</span>
    </g-link>
  </nav>
</template>


<style lang="scss">
.main-nav {
  flex-wrap: nowrap;
}
@media screen and (max-width: 850px) {
 .main-nav {
    order: 10;
    min-width: 100%;
    a {
      padding-top: 5px;
      padding-bottom: 10px;
    }
  }
}
</style>

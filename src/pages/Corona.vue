<template>
  <Layout>
     <Section container="md" class="blog-posts">
      <div class="mb-x2 container-sm text-center">
        <h1>Informasi COVID-19</h1>
        <p style="opacity: .8">Pantau perkembangan COVID-19 melalui tautan berikut:</p>
      </div>
      <div class="grid-cols container container-md grid-cols--3">
        <Card class="sponsor text-center">
          <g-image width="100" src="~/assets/images/corona/logo-gugas.png" alt="Logo Gugas COVID-19"/>
          <p><a href="https://covid19.go.id/"  rel="noopener" target="_blank">Website Resmi COVID-19 Nasional</a></p>
        </Card>
        <Card class="sponsor text-center">
          <g-image width="85" src="~/assets/images/corona/logo-jateng.png" alt="Logo Provinsi Jawa Tengah"/>
          <p><a href="https://corona.jatengprov.go.id/"  rel="noopener" target="_blank">Website Resmi COVID-19 Provinsi Jawa Tengah</a></p>
        </Card>
        <Card class="sponsor text-center">
          <g-image width="75" src="~/assets/images/corona/logo-kudus.png" alt="Logo Kabupaten Kudus"/>
          <p><a href="https://corona.kuduskab.go.id/"  rel="noopener" target="_blank">Website Resmi COVID-19 Kabupaten Kudus</a></p>
        </Card>
      </div>
    </Section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Corona'
  }
}
</script>

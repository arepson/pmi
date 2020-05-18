<template>
  <Layout>
     <Section container="md" class="blog-posts">
       <div class="mb-x2 container-sm text-center">
        <h1>Sambutan Ketua PMI Kabupaten Kudus</h1>
      </div>
      <Card title="Hj Rina Budhy Ariani S.H." class="text-center flex-align-middle">
      <g-image class="author-page__avatar" src="~/assets/images/ketua.jpg" blur="10" width="550" retina="true" alt="The Modern Web Background" /> 
       </Card>
       <br>
      <p>Assalamu’alaikum Warahmatullahi Wabarakaatuh.</p>
        <p>Salam Sejahtera untuk kita semua. Puji syukur kita panjatkan kehadirat Allah SWT atas limpahan rahmat dan karunia-Nya, sehingga Palang Merah Indonesia Kabupaten Kudus secara resmi dapat menerbitkan website ini. Langkah ini menjadi komitmen Kami agar dapat lebih dekat dengan masyarakat Kudus pada khususnya, website ini juga bertujuan sebagai media publikasi dan informasi kegiatan dan bentuk pertanggungjawaban Palang Merah Indonesia Kabupaten Kudus.</p>
        <p>Harapan Kami dengan hadirnya website ini dapat memberikan dampak positif bukan hanya sekedar rutinitas atau melaksanakan kewajiban Kami di organisasi, akan tetapi dapat menciptakan kegiatan yang sifatnya inovatif sehingga PMI kedepannya dapat menjadi organisasi sosial kemasyarakatan yang mampu menjawab tantangan zaman, mampu mewujudkan PMI yang profesional, mandiri, berkarakter dan dicintai masyarakat.</p>
        <p>Dalam menyikapi dan memenuhi tuntutan masyarakat, PMI berupaya memberikan pelayanan terbaik, dengan pelayanan donor darah yang menjadi prioritas yang utama. Demikian kami sampaikan, saran dan kritik yang membangun dari semua pihak kami harapkan demi kemajuan dan peningkatan pelayanan PMI Kabupaten Kudus kedepannya.</p>
        <p>Terima kasih,
        <br>Wassalamualaikum Warahmatullahi Wabarakaatuh.</p>
    </Section>
  </Layout>
</template>

<page-query>
query {
  posts: allBlogPost {
    edges {
      node {
        id
        title
        path
        date (format: "D. MMMM YYYY")
        timeToRead
        author {
          title
          path
          avatar (width: 60)
        }
        excerpt
        content
      }
    }
  }
}
</page-query>

<script>
import PostCard from '@/components/PostCard.vue'

export default {
  components: {
    PostCard
  },
  metaInfo: {
    title: 'Sambutan Ketua'
  }
}
</script>

<style lang="scss">
.author-page {
  &__avatar {
    display: block;
    margin-left: auto;
    margin-right: auto
  }
}
</style>
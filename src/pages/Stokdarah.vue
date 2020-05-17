<template>
  <Layout>
     <Section container="md" class="blog-posts">
      <div class="mb-x2 container-sm text-center">
        <h1>Info Stok Darah</h1>
        <p style="opacity: .8">Jumlah Stok Darah dapat berubah sewaktu-waktu, untuk Info stok darah terkini silahkan menghubungi UDD PMI Kudus melalui telepon.</p>
      </div>
      <iframe src="https://public.tableau.com/views/StokDarah/Sheet1?:embed=y&:display_count=yes&:showVizHome=no" width="100%" height="600" style="border:none"></iframe>  
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
    title: 'Stok Darah'
  }
}
</script>

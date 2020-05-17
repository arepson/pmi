<template>
  <Layout>
     <Section container="md" class="blog-posts">
      <div class="mb-x2 container-sm text-center">
        <h1>Hubungi Kami</h1>
        <p style="opacity: .8">Sampaikan pertanyaan, saran atau kritik Anda melalui kontak dibawah ini:</p>
      </div>
    <div class="grid-cols container container-md grid-cols--2">
    	<Card class="sponsor text-center">
	      <h3>Alamat</h3>
	      <p>Jl. Kudus - Purwodadi (Depan RS Mardi Rahayu), Jati Kulon Kudus</p>
    	</Card>
      <Card class="sponsor text-center">
	      <h3>Telepon</h3>
	      <p>- Markas: <a href="tel:0291437078">(0291) 437078</a>
        <br>- UDD: <a href="tel:0291445689">(0291) 445689</a></p>
    	</Card>
      <Card class="sponsor text-center">
	      <h3>Email</h3>
	      <p><a href="mailto:kab_kudus@pmi.or.id">kab_kudus@pmi.or.id</a></p>
    	</Card>
      <Card class="sponsor text-center">
	      <h3>Facebook</h3>
	      <p><a href="https://www.facebook.com/pmikabkudus/"  rel="noopener" target="_blank">PMI Kabupaten Kudus</a></p>
    	</Card>
      <Card class="sponsor text-center">
	      <h3>Instagram</h3>
	      <p><a href="https://www.instagram.com/pmi.kudus/"  rel="noopener" target="_blank">pmi.kudus</a></p>
    	</Card>
      <Card class="sponsor text-center">
	      <h3>Twitter</h3>
	      <p><a href="https://twitter.com/KudusPmi"  rel="noopener" target="_blank">PMI Kudus</a></p>
    	</Card>
    </div>
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
    title: 'Blog'
  }
}
</script>

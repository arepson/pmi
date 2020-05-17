<template>
  <Layout>
     <Section container="md" class="blog-posts">
      <div class="mb-x2 container-sm text-center">
        <h1>Gridsome Blog</h1>
        <p style="opacity: .8">Follow our mission to make the easiest and most fun framework for building modern websites & apps that are fast by default.</p>
      </div>
      <PostCard v-for="edge in $page.posts.edges" :key="edge.node.id" :post="edge.node"/>
      
        <pagination-posts
        v-if="$page.posts.pageInfo.totalPages > 1"
        base="/berita"
        :totalPages="$page.posts.pageInfo.totalPages"
        :currentPage="$page.posts.pageInfo.currentPage"
      />
      
    </Section>
  </Layout>
</template>

<page-query>
query Posts ($page: Int) {
  posts: allBlogPost (sortBy: "date", order: DESC, perPage: 3, page: $page) @paginate {
    totalCount
    pageInfo {
      totalPages
      currentPage
    }
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
import PaginationPosts from '../components/PaginationPosts'

export default {
  components: {
    PostCard,
    PaginationPosts
  },
  metaInfo: {
    title: 'Berita'
  }
}
</script>

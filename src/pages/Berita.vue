<template>
  <Layout>
     <Section container="md" class="blog-posts">
      <div class="mb-x2 container-sm text-center">
        <h1>Berita PMI Kudus</h1>
        <p style="opacity: .8">#KitaHadapiBersama</p>
      </div>
			<transition-group name="fade">
				<PostCard
					v-for="{ node } of loadedPosts"
					:key="node.id"
					:post="node"
				/>
			</transition-group>
			<ClientOnly>
				<infinite-loading @infinite="infiniteHandler" spinner="spiral">
					<div slot="no-more">
						Kamu sudah mencapai berita terakhir :)
					</div>
					<div slot="no-results">
						Maaf, belum ada berita yang dipublish :(
					</div>
				</infinite-loading>
			</ClientOnly>
    </Section>
  </Layout>
</template>

<page-query>
query ($page: Int) {
	posts: allBlogPost(sortBy: "date", order: DESC, perPage: 3, page: $page) @paginate {
		pageInfo {
			totalPages
			currentPage
		}
    edges {
      node {
        id
        title
        path
        date (format: "D MMMM YYYY")
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
import PostCard from '~/components/PostCard.vue'
export default {
	metaInfo: {
		title: 'Berita'
	},
	components: {
		PostCard
	},
	data() {
		return {
			loadedPosts: [],
			currentPage: 1
		}
	},
	created() {
		this.loadedPosts.push(...this.$page.posts.edges)
	},
		methods: {
		async infiniteHandler($state) {
			if (this.currentPage + 1 > this.$page.posts.pageInfo.totalPages) {
				$state.complete()
			} else {
				const { data } = await this.$fetch(
					`/berita/${this.currentPage + 1}`
				)
				if (data.posts.edges.length) {
					this.currentPage = data.posts.pageInfo.currentPage
					this.loadedPosts.push(...data.posts.edges)
					$state.loaded()
				} else {
					$state.complete()
				}
			}
		}
	}
}
</script>

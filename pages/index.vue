
export { posts };
 <script setup>
 // Replace with the actual library
 
//  const { data: posts, error } = useFetch("http://localhost/shv/wp-json/wp/v2/posts?_embed=1");

 const { data: posts, error } = useFetch(" http://beta.niyogin.com/wp-json/wp/v2/posts?_embed=1");
 // Ensure 'posts' is exposed for use in the template

 </script>


  <template>
    <div>
      <ProfileHeader />
  
      <section class="container py-16">
        <div v-if="posts && posts.length" class="grid sm:grid-cols-3 gap-5">
          <div v-for="post in posts" :key="post.id" class="bg-white p-6 shadow-md rounded-md">
            <!-- Your BlogCard content goes here -->
            <h2 class="text-xl font-bold mb-4">{{ post.title.rendered }}</h2>
            <!-- Add more content as needed ? -->
            <img v-if="post.featured_media" :src="post._embedded['wp:featuredmedia'][0]?.source_url" alt="Blog Image" class="mb-4 rounded-md">
            <!-- Example: Link to the blog post using the slug -->
            <router-link :to="'/' + post.slug" class="text-blue-500 hover:underline">Read more</router-link>
          </div>
        </div>
  
        <div v-else class="text-center text-gray-600">
          <!-- Add a message or loader when posts are not available -->
          Loading posts...
        </div>
      </section>
    </div>
  </template>
  
 
  
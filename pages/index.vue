<template>
<div class="contents">
  <ul>
    <li v-for="content in contents" :key="content.id">
      <nuxt-link :to="`/${content.id}`">
      {{ content.title }}
      </nuxt-link>
      {{ new Date(content.publishedAt).toLocaleDateString() }}
    </li>
  </ul>
</div>
</template>
<script>
import axios from 'axios'
export default {
async asyncData() {
const { data } = await axios.get(
// your-service-id
'https://neskblog.microcms.io/api/v1/blog',
{
// your-api-key
headers: { 'X-API-KEY': 'c7ad9a8b-095d-47ca-a933-2af56bc189dc' }
}
)
return data
}
}
</script>

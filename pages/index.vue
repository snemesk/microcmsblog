<template>
<div class="contents">
    <section class="bar background-image-fixed-2 no-mb color-white text-center">
    <div class="dark-mask"></div>
    <div class="container">
        <div class="row">
            <div class="col-md-12">
                <h3>テキスト</h3>
                <p class="lead">さぶたいとる</p>

            </div>
        </div>
    </div>
  </section>
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

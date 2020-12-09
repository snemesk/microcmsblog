<template>
<section class="bar background-image-fixed-2 no-mb color-white text-center">
    <div class="dark-mask"></div>
    <div class="container">
        <div class="row">
            <div class="col-md-12">
                <!--<div class="icon icon-lg"><i class="{{ .Site.Params.see_more.icon }}"></i>
                </div>-->
                <br>
                <br>
                <br>
                <br>
                <br>
                <h3>{{ .Site.Params.see_more.title | markdownify }}</h3>
                <p class="lead">{{ .Site.Params.see_more.subtitle | markdownify }}</p>
                <p class="text-center">
                    {{ with .Site.Params.see_more.link_url }}
                     <a href="{{ . }}" class="btn btn-template-transparent-black btn-lg">
                    {{ end }}
                        {{ with .Site.Params.see_more.link_text }}
                        {{ . | markdownify }}
                        {{ end }}
                    {{ with .Site.Params.see_more.link_url }}
                    </a>
                    {{ end }}
                </p>
                <br>
                <br><br>
                <br>
                <br>
            </div>
        </div>
    </div>
</section>

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

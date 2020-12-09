<template>
<div class="contents">
    <section class="bar background-image-fixed-2 no-mb color-white text-center">
    <div class="container">
        <div class="row">
                <h3>テキスト</h3>
                <p class="lead">さぶたいとる</p>
        </div>
    </div>
  </section>
  <section class="bar background-white">
    <div class="container">
        <div class="col-md-12">
            <div class="row">
                <div class="col-md-4">
                    <div class="box-simple">
                        <a href="">
                            <div class="icon">
                                <i class=""></i>
                            </div>
                        </a>
                        <h3></h3>
                        <p></p>
                    </div>
                </div>
            </div>
        </div>
    </div>
  </section>
  <section class="blog">
  <ul>
    <li v-for="content in contents" :key="content.id">
      <nuxt-link :to="`/${content.id}`">
      {{ content.title }}
      </nuxt-link>
      {{ new Date(content.publishedAt).toLocaleDateString() }}
    </li>
  </ul>
  </section>
  <section>
<a class="twitter-timeline" href="https://twitter.com/obisuki_food?ref_src=twsrc%5Etfw">Tweets by obisuki_food</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
  </section>
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

<style lang="scss" scoped>
.bar.background-image-fixed-2 {
    background: url();
    background-size: cover;
    background-position-y: 50%;
}

.bar {
    position: relative;
    background: #858b92;
    padding: 60px 0;
}
.no-mb {
    margin-bottom: 0 !important;
}
.text-center {
    text-align: center;
}
article, aside, details, figcaption, figure, footer, header, hgroup, main, menu, nav, section, summary {
    display: block;
}
* {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}
user agent stylesheet
section {
    display: block;
}
.blog{
  width: 800px;
  margin: auto;
}
</style>

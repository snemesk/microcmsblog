<template>
<div>
      <section class="bar background-image1 no-mb color-white text-center">
        <div >
          <h1>テスト</h1>
        </div>
      </section>
  <div id="content">
    <div class="container">
        <div class="heading text-center">
          <h2>一覧</h2>
        </div>
            <div class="col-md-12">
                          <div class="row">

        <div class="col-md-4" v-for="content in contents" :key="content">
            <a class="card__cover" href="/{{ content.id }}">
            <picture v-if="content.thumbnail">
            <img
            :src="`${content.thumbnail.url}?w=350`"
            class=""
            alt
            />
            </picture>
            </a>
            <div class="card__content">
              <h5 class="card__content-category"></h5>
              <nuxt-link class="card__content-title" :to="`/${content.id}`">
              {{ content.title }}
            </nuxt-link>
              <div class="card__content-info">
                <div class="info__time">
                  <p><i class="far fa-clock"></i>{{ new Date(content.publishedAt).toLocaleDateString() }}</p>
                </div>
            </div>
          </div>
        </div>
  <v-card class="mx-auto">
    <v-card-title>
      <v-icon large left color="#26c6da">twitter</v-icon>
    </v-card-title>
    <v-flex xs12>
      <Timeline :id="user_id" sourceType="profile" :options="{ tweetLimit: '3' }"/>
    </v-flex>
  </v-card>
        </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {Timeline} from 'vue-tweet-embed'
import axios from 'axios'
export default {
  components: {
    Timeline
  },
  data: function() {
    return {
      user_id: "obisuki_food"
    };
  },

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
},
}
</script>


<style lang="scss" scoped>
.bar {
    position: relative;
    background: #858b92;
    padding: 300px 0;
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
section {
    display: block;
}
.blog{
  width: 800px;
  margin: auto;
}
.background-image1 {
  background-image: url("~@/assets/images/backgrounds/toppic001.jpg");
  background-attachment: fixed;
  background-size: cover;
  background-repeat:no-repeat;
  background-position:center center;
}
</style>

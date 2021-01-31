<template>
  <div>
      <section class="bar background-image1 no-mb color-white text-center">
        <div class="heading backgroundfont">
          <h3>Obisuki</h3>
          <p>助け合う。助けたい人に知らせが届くように。</p>
        </div>
      </section>
  <div id="content">
    <div class="container">
        <div class="heading text-center">
          <h3>News一覧</h3>
        </div>
        <div class="row">
          <div class="col-md-4" v-for="content in contents" :key="content">
            <div class="microcms">
              <a class="card__cover" :href="`{{ content.id }}`">
                <picture v-if="content.thumbnail">
                  <img　:src="`${content.thumbnail.url}?w=200`"class=""alt/>
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
            </div>
            </div>
              <div class="col-md-6 offset-md-3">
                <v-card class="mx-auto">
                <v-card-title>
                <v-icon large left color="#26c6da">mdi-twitter</v-icon>
                </v-card-title>
                <v-flex xs12>
                  <Timeline :id="user_id" sourceType="profile" :options="{ tweetLimit: '2' }"/>
                </v-flex>
                </v-card>
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
    padding: 250px 20px;
}
.heading h3 {
  font-size: 24px;
  margin-bottom: 20px;
}

.backgroundfont{
  color: white;
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
.container{
      padding-bottom: 100px;
}
</style>

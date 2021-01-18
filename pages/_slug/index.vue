<template>
<div id="content" class="breadcrumb-pd">
<main class="main">
<picture v-if="thumbnail">
<source
    media="(min-width: 768px)"
    type="image/webp"
    :srcset="`${thumbnail.url}?w=600&fm=webp, ${thumbnail.url}?w=1200&fm=webp 2x`"
    />
<source
    media="(max-width: 768px)"
    type="image/webp"
    :srcset="`${thumbnail.url}?w=375&fm=webp, ${thumbnail.url}?w=750&fm=webp 2x`"
    />
<img
    :src="`${thumbnail.url}?w=1200`"
    class="thumbnail"
    alt
/>
</picture>
<p class="publishedAt">{{ new Date(publishedAt).toLocaleDateString() }}</p>
<h1 class="title">{{ title }}</h1>
<p class="category">{{ category && category.name }}</p>
<div class="post" v-html="body"></div>
</main>
</div>
</template>

<script>
import axios from 'axios'
export default {
async asyncData({ params }) {
const { data } = await axios.get(
`https://neskblog.microcms.io/api/v1/blog/${params.slug}`,
{
headers: { 'X-API-KEY': 'c7ad9a8b-095d-47ca-a933-2af56bc189dc' }
}
)
return data
}
}
</script>
<style lang="scss" scoped>
.category{
    background-color: #467fbf;
    color: #ffffff;
    right: 0;
    padding-left: 10px;
    padding-right: 10px;
    text-transform: none;
    letter-spacing: 0.08em;
    font-weight: 300;
    font-size: 12px;
    opacity: 0.7;
    display: inline-block;
    text-align: left;

}
.content{
    padding-top: 80px;
}
.main {
  width: 960px;
  margin-top:20px;
  margin: 0 auto;
  padding:0 20px;
}

.title {
  margin-bottom: 20px;
}
h1{
  font-size: 30px;
  font-weight: bold;
  margin: 40px 0 20px;
  padding: 10px 20px;
  border-radius: 5px;
  }

.publishedAt {
margin-bottom: 40px;
text-align: left;
}
.post {
  text-align: left;
  margin: auto;

.twitter-tweet{

}
h1 {
  font-size: 30px;
  font-weight: bold;
  margin: 40px 0 20px;
  background-color: #eee;
  padding: 10px 20px;
  border-radius: 5px;
  }
h2 {
  font-size: 24px;
  font-weight: bold;
  margin: 40px 0 16px;
  border-bottom: 1px solid #ddd;
}
p {
  line-height: 1.8;
  letter-spacing: 0.2px;
}
ol {
  list-style-type: decimal;
  list-style-position: inside;
  }
}
</style>

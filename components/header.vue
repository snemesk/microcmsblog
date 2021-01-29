<template>
    <header>
      <div class="container">
        <div class="header-wrapper">
          <div class="title">
            <nuxt-link :to="`/`">Obisuki</nuxt-link>
          </div>
          <nav>
            <ul>
              <li class="nav-item">
                <nuxt-link :to="`/`">Home</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link :to="`/about`">About</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link :to="`/contact`">Contact</nuxt-link>
              </li>
            </ul>
          </nav>
          <div class="header__icon-group">
            <div class="social">
              <a href="https://twitter.com/obisuki_food"><i class="fab fa-twitter-square"></i></a>
            </div>
          </div>
        </div>
      </div>
    </header>
</template>

<style scoped>
.title{
    color: #111;
    font-size: 1em;
    font-weight: 600;
    text-decoration: none;
    line-height: 1em;
    cursor: pointer;
    transition: .2s ease-in-out;
    position: relative;
    padding: 8px 0;
    overflow: hidden;
    display: inline-block;
}
</style>

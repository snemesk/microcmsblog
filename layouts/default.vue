<template>
  <div>
  <div class="top">
      <div class="header__flex">
        <NuxtLink to="/">
          <h1>Obisuki</h1>
        </NuxtLink>
    <nav>
      <ul>
        <li>
          <NuxtLink to="/about">このサイトについて</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/contact">問い合わせ</NuxtLink>
        </li>
      </ul>
    </nav>
  </div>
    <div class="navtop">

    <nav>
    <div class="nav">
      <ul>
      </ul>
    </div>
    </nav>
    </div>
  </div>
    <Nuxt />
  </div>
</template>

<style>
  * {
 margin: 0;
 padding: 0;
}
ul {
  list-style:none;
}

.header__flex {
  display: flex;
  height:60px;
  align-items: center;
}
.header__flex nav {
  margin-left: auto;
}
.header__flex ul {
  display: flex;
}
.header__flex ul li {
  margin-left: 20px;
}

.top {
  width: 1200px;
  margin: auto;
  background: lightskyblue;
}
.navtop {
  max-width: 1100px;
  margin: auto;
}
ul {
  list-style:none;
}
.nav {
  display: flex;
  align-items: center;
}
.nav nav {
  margin-left: auto;
}
.nav ul {
  display: flex;

  li:first-child {
    margin-right: auto;
  }
}
.nav ul li {
  margin-left: 20px;
}

html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>

<template>
    <header>
      <div class="container">
        <div class="header-wrapper"><a class="header__logo" href="/">test</a>
          <nav>
            <ul>
              <li class="nav-item"><a href="/">Home</a>
              </li>
              <li class="nav-item"><a href="/">Pages</a>
              </li>
              <li class="nav-item"><a href="/about">About</a></li>
            </ul>
          </nav>
          <div class="header__icon-group">
            <div class="social">
              <a href="https://twitter.com/2MByte_nesk"><fa :icon="faTwitter" /></a>
            </div>
          </div>
        </div>
      </div>
    </header>
</template>

<script>
import { faTwitter } from '@fortawesome/free-brands-svg-icons'
export default {
  computed: {
    faTwitter () {
      return faTwitter
    }
  }
}
</script>

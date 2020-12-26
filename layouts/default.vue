<template>
  <div>
    <Header />
    <main>
      <Nuxt />
    </main>
    <Footer />
  </div>
</template>

<script>
	import Header from "@/components/header.vue"; // headerをインポート
  import Footer from "@/components/footer.vue"; // footerをインポート
	export default {
		components: {
			Header,
      Footer,
		}
	}
</script>
<style>
* {
 margin: 0;
 padding: 0;
}
	main {
		min-height: 600px;
		background-color: #ddd;
		text-align: center;
	}
	.page-enter-active,
	.page-leave-active {
		transition: 0.5s cubic-bezier(1, 0.25, 0.25, 1);
	}
	.page-enter,
	.page-leave-active {
		opacity: 0;
		transform: translate(0, 30px);
	}

ul {
  list-style:none;
}

.header__flex {
  display: flex;
  height:60px;
  align-items: center;
  width: 1000px;
  margin: auto;
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

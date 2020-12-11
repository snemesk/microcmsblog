<template>
	<div>
		<nav>
			<ul>
				<li>
					<nuxt-link to="/about">Obisukiとは</nuxt-link>
				</li>
				<li>
					<nuxt-link to="/page1">リンク2</nuxt-link>
				</li>
				<li>
					<nuxt-link to="/page2">リンク3</nuxt-link>
				</li>
				<li>
					<nuxt-link to="/page3">リンク4</nuxt-link>
				</li>
			</ul>
		</nav>
	</div>
</template>
<script>
	export default {
		components: {}
	};
</script>
<style lang="scss" scoped>
nav {
	ul {
		display: flex;
		justify-content: flex-end;
		li {
			list-style-type: none;
			margin-left: 15px;
		}
	}
}
</style>

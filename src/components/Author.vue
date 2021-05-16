<template>
	<div class="author">

		<h1 v-if="showTitle" class="author__site-title">
			{{ $static.metadata.siteName }}
		</h1>

		<p class="author__intro">
			A simple site for Salvation Army Stoneycroft to blog and share sermons.
		</p>

		<p>
		<iframe src=https://anchor.fm/oldswanchurch/embed height=102px
		width=100% frameborder=0 scrolling=no></iframe>

		</p>

		<p class="author__links">
			<a href="https://anchor.fm/oldswanchurch">Sermons</a>
			<a href="https://youtube.com/channel/UCXA3SpX5Iz-aSLY0U7CA2Bg">YouTube</a>
			<a href="https://gitlab.com/oldswanchurch/website">GitLab</a>
		</p>

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding-bottom: calc(var(--space) / 2);

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		margin: 0 auto;
		font-size: 1.5em;
		max-width: 400px;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>

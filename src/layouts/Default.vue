<template>
	<div class="layout">
		<header class="header">
			<strong>
				<g-link to="/">{{ $static.metadata.siteName }}</g-link>
			</strong>
			<nav class="nav">
				<g-link class="nav__link" to="/">Home</g-link>
				<g-link class="nav__link" to="/registration/"
					>Registration</g-link
				>
			</nav>
		</header>
		<slot />
	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");
body {
	font-family: "Poppins", sans-serif !important;
	margin: 0;
	padding: 0;
	line-height: 1.5;
}

.layout {
	width: 100%;
	max-width: 1200px;
	margin: 0 auto;
	padding-left: 20px;
	padding-right: 20px;
}

.header {
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 20px;
	height: 80px;
}

.nav__link {
	margin-left: 20px;
}
</style>

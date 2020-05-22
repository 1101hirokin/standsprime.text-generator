<template>
	<div>
		<nuxt />
	</div>
</template>

<style lang="scss">


$aspectRatio: 210/(297 + 3);
$width: 900px;
section {
	margin: 10px auto;

	width: $width;
	height: $width*$aspectRatio;

	overflow: hidden;
	box-shadow: 0px 3px 6px rgba(0,0,0, .3);

	background-color: white;

	position: relative;
}
@media print {
	@page {
		size: ($width) ($width*$aspectRatio);
	}
	* {
		-webkit-print-color-adjust: exact;
	}
	body {
		margin: 0;
		background-color: #ffffff;
	}
	section {
		margin: 0;
		box-shadow: none;
		page-break-before: always;
	}
}

html {
	font-family: "Helvetica Neue", Arial, "Hiragino Kaku Gothic ProN",  "Hiragino Sans", Meiryo, sans-serif;
	font-size: 16px;
	word-spacing: 1px;
	-ms-text-size-adjust: 100%;
	-webkit-text-size-adjust: 100%;
	-moz-osx-font-smoothing: grayscale;
	-webkit-font-smoothing: antialiased;
	box-sizing: border-box;
}

*,
*:before,
*:after {
	box-sizing: border-box;
	margin: 0;
}

body {
	margin: 0;
	background-color: #eaeaea;
}
</style>

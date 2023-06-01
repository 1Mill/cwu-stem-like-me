<template>
	<main style="display: flex; flex-direction: column; align-items: center; gap: 1rem;">
		<h1>STEM Like Me</h1>
		<div :style="style"/>
		<section>
			<button @click="() => resetStyle()">
				Reset
			</button>
		</section>
		<section>
			<button @click="() => addStyle({ backgroundColor: 'CornflowerBlue' })">
				Erik's Color
			</button>
			<button @click="() => addStyle({ cursor: 'grab' })">
				Erik's Cursor
			</button>
			<button @click="() => addStyle({ borderRadius: '10%', transform: 'skew(20deg)rotate(30deg)' })">
				Erik's Shape
			</button>
		</section>

		<p>EEEE</p>

		<!-- List of valid colors -->
		<!-- https://www.w3schools.com/cssref/css_colors.php -->
		<section>
		</section>
	</main>
</template>

<script>
const DEFAULT_STYLE = {
	backgroundColor: 'black',
	height: '100px',
	padding: '1rem',
	width: '100px',
}

console.log("Hello World!")

export default {
	data: function () {
		return { style: DEFAULT_STYLE }
	},
	methods: {
		addStyle: function (style) {
			this.style = {
				...this.style,
				...style,
			}
		},
		resetStyle: function() {
			this.style = DEFAULT_STYLE
		}
	}
}
</script>

<style scoped>
	section {
		align-content: center;
		display: flex;
		flex-wrap: wrap;
		gap: 0.5rem;
	}
</style>

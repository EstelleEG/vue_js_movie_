<template>
	<div>
		<div class="courses-container">
			<div class="course">
				<div class="course-preview">
					<img :src="movie.image" alt="affiche" />
				</div>
				<div class="course-info">
					<h2>{{ movie.title }}</h2>
					<h6>{{ movie.release_date }}</h6>
					<span>autre info</span>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import axios from 'axios'

export default {
	name: 'FilmDetails',
	data: () => ({
		movie: {}
	}),
	async created() {
		const { filmId } = this.$route.params
		const apiDetailsUri = 'https://ghibliapi.herokuapp.com/films/' + filmId
		const oneMovie = await axios.get(apiDetailsUri)
		this.movie = oneMovie.data
		console.log(oneMovie)
	}
}
</script>
<style scoped>
.courses-container {
	font-family: "Muli", sans-serif;
	display: flex;
	align-items: center;
	justify-content: center;
	color: black;
	flex-direction: column;
}

.course {
	background-color: #fff;
	border-radius: 10px;
	box-shadow: 0 10px 10px rgba(0, 0, 0, 0.2);
	display: flex;
	max-width: 100%;
	margin: 20px;
	overflow: hidden;
	width: 700px;
}

.course h6 {
	opacity: 0.6;
	margin: 0;
	letter-spacing: 1px;
	text-transform: uppercase;
}

.course h2 {
	letter-spacing: 1px;
	margin: 10px 0;
}

.course-preview {
	background-color: cyan;
	color: #fff;
	padding: 30px;
	max-width: 250px;
}
.course-preview img {
	max-height: 250px;
}
.course-preview a {
	color: #fff;
	display: inline-block;
	font-size: 12px;
	opacity: 0.6;
	margin-top: 30px;
	text-decoration: none;
}

.course-info {
	padding: 30px;
	position: relative;
	width: 100%;
}

.btn {
	background-color: #2a265f;
	border: 0;
	border-radius: 10px;
	box-shadow: 0 10px 10px rgba(0, 0, 0, 0.2);
	color: #fff;
	font-size: 16px;
	padding: 12px 25px;
	position: absolute;
	bottom: 30px;
	right: 30px;
	letter-spacing: 1px;
}
</style>

<template>
	<div class="main-container tw-flex tw-flex-col ">
		<div class="blue-banner tw-container-fluid tw-flex tw-flex-wrap tw-content-center">
			<div class="tw-container tw-content-center tw-text-white tw-mx-auto tw-p-3 tw-flex tw-flex-row tw-justify-around tw-grid lg:tw-grid-cols-2 sm:tw-grid-cols-2">
				<div class="tw-flex tw-flex-row  tw-content-center tw-justify-center">
					<v-icon color="white">mdi-email</v-icon>
					<p class="tw-ml-3">johenelpl@gmail.com</p>
				</div>
				<div class="tw-flex tw-flex-row tw-content-center  tw-justify-center">
					<v-icon color="white">mdi-phone</v-icon>
					<p class="tw-ml-3">+ 639 - 771 - 120 - 853</p>
				</div>
			
			</div>
			<!-- <div class="tw-container tw-mx-auto tw-text-white tw-p-1">
				<navigation></navigation>
			</div> -->
		</div>
		<div class="tw-container tw-shadow tw-mx-auto tw-flex tw-flex-col" style="min-height: 100vh">
			<div class="section section-introduction">
				<introduction/>
			</div>
			<div class="section section-skills  tw-flex tw-flex-col">
				<header class="tw-mb-24">Skills</header>
				<techstack/>
			</div>
			<div class="section section-career tw-flex tw-flex-col" style="padding-top:">
				<header>Career</header>
				<career/>
			</div>
			<div class="section section-portfolio tw-grid tw-grid-cols-1" style="background:#fbfbfb;overflow:auto">
				<header>Portfolio</header>
				<portfolio class="tw-mt-5 tw-mx-auto"/>
			</div>
		</div>
		<footer>

		</footer>
	</div>
</template>

<script>
// import Navigation from './Navigation';
import Introduction from './Introduction';
import TechStack from './TechStack';
import Career from './Career';
import Portfolio from './Portfolio';

export default {
	name: 'Johenel',
	components: {
		// navigation: Navigation,
		introduction: Introduction,
		techstack: TechStack,
		career: Career,
		portfolio: Portfolio
	}
}
</script>

<style scoped>
	p {
		margin: 0;
	}
	header {
		font-size:1.5rem;
		border: 2px grey solid;
		width: fit-content;
		@apply border bg-gray-100 text-gray-700 px-5;
	}
	footer {
		height: 2rem;
		@apply tw-bg-blue-900 mt-10;
	}
	.main-container {
		min-height: 100vh;
	}

	.blue-banner {
		@apply tw-bg-blue-800;
		width: 100vh;
		height: 3rem;
	}
	
	.section {
		@apply tw-p-6 tw-flex tw-flex-wrap tw-content-center;
		min-height: 28rem;
	}

	@media(max-width: 768px) {
		.blue-banner {
			height: 4.5rem
		}
	}
</style>

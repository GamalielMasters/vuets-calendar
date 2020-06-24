<template>
	<div id="app">
		<div id="header">
			<div>
				<img alt="Vue logo" src="../assets/logo.png">
				<h1>Vue-Ts Calendar</h1>
			</div>
		</div>
		<calendar :month="currentMonth"/>
	</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import moment from 'moment';
import Calendar from '@/components/Calendar.vue';

@Component({
	components: {
		Calendar,
	},
})
export default class App extends Vue {
	currentMonth : moment.Moment = moment()
}
</script>

<style lang="scss">
@import "@/styles/_globals.scss";

#header {
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: flex-end;

	div:first-child {
		display: flex;
		flex-direction: row;
		align-items: center;
		margin: 1rem 0;
		img {
			width: 50px;
			height: 50px;
		}
		h1 {
			margin: 0 0 0 0.5rem;
			color: $pickled-bluewood;
			padding-top: 7px;
		}
	}

	div:last-child {
		font-weight: bold;
		button {
			color: $dusty-gray;
			font-size: 1rem;
			padding: 0;
			width: 20px;
			background-color: white;
			user-select: none;
			border: 1px solid $alto;
			border-radius: 2px;
			margin-left: 0.25rem;
			&:focus {
				outline: none;
			}
			&:hover {
				color: $pickled-bluewood;
				box-shadow: 0 2px 2px $alto;
			}
		}
	}
}

</style>

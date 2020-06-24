<template>
	<div id="calendar">

		<calendar-week v-for="week in Weeks" :start-of-week="week" v-bind:key="week"></calendar-week>
	</div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import moment from 'moment';

import CalendarWeek from '@/components/CalendarWeek.vue';

@Component({
	components: {
		CalendarWeek,
	},
})
export default class Calendar extends Vue {
	@Prop({ default: moment.utc().month() }) month !: moment.Moment;

	get CalendarBegin() : moment.Moment {
		const firstOfTheMonth: moment.Moment = this.month.clone().date(1);
		return firstOfTheMonth.day('Monday');
	}

	Weeks : moment.Moment[] = [0, 1, 2, 3, 4].map(val => this.CalendarBegin.add(val, 'weeks'))
}
</script>

<style scoped lang="scss">
#calendar {
  background-color: white;
}
</style>

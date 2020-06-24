<template>
  <div class="calendar-week">
	  <calendar-day v-for="day in Days" :day="day"></calendar-day>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import moment from 'moment';
import CalendarDay from '@/components/CalendarDay.vue';

@Component({
    components: {
    	CalendarDay,
    },
})
export default class CalendarWeek extends Vue {
	@Prop() startOfWeek !: moment.Moment;

	get Days() : moment.Moment[] {
		return [0, 1, 2, 3, 4, 5, 6].map((val) => { return this.startOfWeek.clone().add( val, 'days' ) })
	}
}
</script>

<style scoped lang="scss">
  @import "@/styles/_globals.scss";

  .calendar-week {
    @include calendar-row;
  }
</style>

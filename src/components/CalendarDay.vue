<template>
  <div class="day" :class="{ past: isPast, 'not-current-month': !isCurrentMonth, today: isToday }">
    <p>{{Day.date()}}</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import moment from 'moment';

@Component
export default class CalendarDay extends Vue {
	@Prop() Day !: moment.Moment;

	get isCurrentMonth(): boolean {
		return this.Day.month() === moment().month();
	}

	get isPast() : boolean {
		return this.Day.isBefore(moment(), 'day');
	}

	get isToday() : boolean {
		return this.Day.isSame(moment(), 'day');
	}
}
</script>

<style scoped lang="scss">
@import '@/styles/_globals';
.day {
  overflow: hidden;
  font-weight: bold;
  @include calendar-cell;
  height: 100px;
  user-select: none;
  cursor: default;
  border-left: $calendar-border;
  border-top: $calendar-border;

  &:last-child {
    border-right: $calendar-border;
  }

  &.past {
    opacity: 0.6;
  }

  &.not-current-month {
    color: $alto;
  }

  &.today {
    background-color: $buttermilk;
  }

  &.active {
    background-color: $pink;
  }

  .event-list {
    font-size: 0.8rem;
    color: $vista-blue;
    font-weight: bold;
    list-style: none;
    padding: 0;
    margin: 0.5rem 0 0.5rem 0;

    li {
      white-space: nowrap;
    }
  }
}

.calendar-week{
  &:last-child {
    .day {
      border-bottom: $calendar-border;
    }
  }
}
</style>

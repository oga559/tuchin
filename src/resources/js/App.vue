<template>

</template>

<script lang="js">
import moment from "moment";

export default {
    getCalendar() {
    let startDate = this.getStartDate();
    const endDate = this.getEndDate();
    const weekNumber = Math.ceil(endDate.diff(startDate, "days") / 7);

    let calendars = [];
    for (let week = 0; week < weekNumber; week++) {
      let weekRow = [];
      for (let day = 0;  day < 7; day++) {
        weekRow.push({
          date: startDate.get("date"),
        });
        startDate.add(1, "days");
      }
      calendars.push(weekRow);
    }
    return calendars;
  },
  mounted(){
    console.log(this.getCalendar());
  }
}
</script>

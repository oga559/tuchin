<template>
  <div>a</div>
</template>

<script lang="ts">
import moment from "moment";

export default {
  mounted(){
    let date = moment().startOf("month");
    const youbiNum = date.day();
    console.log(youbiNum)
  }
};
</script>

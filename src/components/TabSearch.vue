<template>
  <div>
    <date-picker
      language="en"
      apply-button-label="use"
      :show-helper-buttons="true"
      :switch-button-initial="true"
      :is-monday-first="true"
      :date-input="{
        inputClass: 'date_input',
      }"
      :calendar-time-input="{
        readonly: true,
        step: 30,
        inputClass: 'calendar_time_input',
      }"
    ></date-picker>
  </div>
</template>

<style scoped>
.vdpr-datepicker .calendar_time_input {
  background-color: aqua !important;
}

.vdpr-datepicker .date_input {
  border: 1px solid red;
  width: 400px;
  height: 80px;
  margin-bottom: 25px;
}
</style>

<script>
import DatePicker from "./TimeRangerPicker.vuexxx";

export default {
  setup() {},
  components: {
    DatePicker,
  },
};
</script>

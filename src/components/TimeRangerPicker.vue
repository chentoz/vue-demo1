<template>
  <div>
      <label>日期范围</label>
  </div>
</template>

<script>
import DatePicker, {
  CalendarDialog,
} from "vue-time-date-range-picker/dist/vdprDatePicker";

import "vue-time-date-range-picker/dist/vdprDatePicker.min.css";

export default {
  components: {
    DatePicker,
    CalendarDialog,
  },
};
</script>


<template>
  <h1>TEST</h1>
  <b-field label="Select a date">
    <b-datepicker
      placeholder="Click to select..."
      :min-date="minDate"
      :max-date="maxDate"
    >
    </b-datepicker>
  </b-field>
</template>

<script>
export default {
  name: "customDate",
  data() {
    const today = new Date();

    return {
      date: new Date(),
      minDate: new Date(
        today.getFullYear() - 1,
        today.getMonth(),
        today.getDate()
      ),
      maxDate: new Date(
        today.getFullYear() + 18,
        today.getMonth(),
        today.getDate()
      ),
    };
  },
};
</script>



<template>
  <v-date-picker
    @input="handleChange"
    :min="min"
    no-title
    next-icon="mdi-menu-right"
    prev-icon="mdi-menu-left"
    color="primary"
    elevation="1"
    :full-width="fullWidth"
    v-model="selectedBookingDate"
  ></v-date-picker>
</template>
<script>
export default {
  name: "BadDatePicker",
  data() {
    return {
      selectedBookingDate: this.value
    };
  },
  methods: {
    handleChange() {
      this.$emit("input", this.selectedBookingDate);
    }
  },
  props: {
    min: String,
    fullWidth: {
      type: Boolean,
      default: false
    }
  }
};
</script>
<style scoped></style>

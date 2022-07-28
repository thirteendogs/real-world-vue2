<template>
  <div>
    <h1>Hi from EventList view</h1>
    <EventCard />
  </div>
</template>

<script>
import EventCard from "@/components/EventCard.vue";

export default {
  components: {
    EventCard,
  },
};
</script>

<style lang="scss" scoped></style>

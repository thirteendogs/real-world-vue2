<template>
  <div>
    <h1>Hi from EventList view</h1>
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
import EventCard from "@/components/EventCard.vue";
import EventService from "@/services/EventService.js";
export default {
  components: {
    EventCard,
  },
  data() {
    return {
      events: [],
    };
  },
  created() {
    EventService.getEvents()
      .then((response) => {
        this.events = response.data;
        console.log(this.events);
      })
      .catch((error) => {
        console.log("We encountered this error", error.response);
      });
  },
};
</script>

<style lang="scss" scoped></style>

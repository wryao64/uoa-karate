
<template>
  <div class="events-container">
    <div class="">
      <h2 class="event-title">Upcoming Events:</h2>
      <p class="page-desc">
        This page lists upcoming club events. Events range from casual social gatherings to training camps in other cities or even other countries. There is no guarantee it is up to date.
        This page was last updated on 23/03/2019. If you have any questions about upcoming events you can find a <router-link to="/">contact form here</router-link>.
      </p>
    </div>
    <div
      v-for="event in eventList"
      :key="event.name"
      class="event"
    >
      <EventComponent :event="event" />
    </div>
  </div>
</template>

<script>
import eventList from "@/assets/events.json";
import EventComponent from "@/components/EventComponent";

export default {
  name: "EventsView",
  components: {
    EventComponent
  },
  data: function() {
    return {
      eventList: eventList
        .filter(event => {
          if (new Date(event.startDate) > new Date()) {
            return true;
          }
        })
        .sort((a, b) => {
          return new Date(a.startDate) - new Date(b.startDate);
        })
    };
  }
};
</script>

<style scoped>
.events-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(auto, 600px));
  grid-auto-rows: minmax(200px, auto);
  grid-gap: 30px;
  grid-auto-flow: dense;
  justify-content: center;
  margin-bottom: 100px;
  min-height: 100vh;
}

.event {
}

.page-desc {
}
</style>

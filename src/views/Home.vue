<template>
  <h1>Events For Good</h1>
  <div class="events">
    <EventCard v-for="event in events" :key="event.id" :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from "@/components/EventCard.vue";

export default {
  name: "Home",
  components: {
    EventCard
  },
  data(){
    return { 
      events: [
       {
        id: 5928101,
        category: 'animal welfare',
        title: 'Cat Adoption Day',
        description: 'Find your new feline friend at this event',
        location: 'Meow Town',
        date:'January 28,2022',
        time:'12:00',
        petsAllowed: true,
        organizer: 'Kat Laydee'
      },
      {
        id: 5928102,
        category: 'animal welfare',
        title: 'Party with your pets',
        description: 'Have a good time with your friends and pets',
        location: 'Bogotá',
        date:'may 4,2022',
        time:'3:00',
        petsAllowed: true,
        organizer: 'Disco stu'
      },
      {
        id: 5928103,
        category: 'webinar',
        title: 'Are cats the new gods?',
        description: 'A discusson about the cateology',
        location: 'New York',
        date:'dec 15,2022',
        time:'4:00',
        petsAllowed: false,
        organizer: 'MIT'
      }
      ]
    }
  }
};
</script>

<style scoped>
.events{
  display:flex;
  flex-direction: column;
  align-items: center;
}
</style>


      
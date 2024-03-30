<script setup>
import { ref } from 'vue'
import { ScheduleXCalendar } from "@schedule-x/vue";
import {
  createCalendar,
  viewDay,
  viewWeek,
  viewMonthGrid,
  viewMonthAgenda,
} from '@schedule-x/calendar'
import '@schedule-x/theme-default/dist/index.css'
import { createResizePlugin } from "@schedule-x/resize";
import { createDragAndDropPlugin } from '@schedule-x/drag-and-drop'
import { createEventModalPlugin } from '@schedule-x/event-modal'
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'


onMounted(() => {
  initFlowbite();
})

const calendarApp = createCalendar({
  selectedDate: '2024-03-19',
  views: [viewDay, viewWeek, viewMonthGrid, viewMonthAgenda],
  defaultView: viewWeek.name,
  plugins: [
    createResizePlugin(),
    createDragAndDropPlugin(),
    createEventModalPlugin()
  ],
  events: [
    {
      id: 1,
      title: 'Event 1',
      start: '2024-03-19 03:00',
      end: '2024-03-19 04:00',
      description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry standard dummy text',
      location: 'Delli, India'
    },
    {
      id: 2,
      title: 'Event 2',
      start: '2024-03-20 03:00',
      end: '2024-03-20 13:00',
      description: 'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old.',
      location: 'Mumbai, India',
    },
    {
      id: 3,
      title: "Event 3",
      start: "2024-03-04 10:00",
      end: "2024-03-04 12:00",
      description: "This is event 3 description.",
      location: "Bangalore, India"
    },
    {
      id: 4,
      title: "Event 4",
      start: "2024-03-08 15:00",
      end: "2024-03-08 16:30",
      description: "This is event 4 description.",
      location: "Chennai, India"
    },
    {
      id: 5,
      title: "Event 5",
      start: "2024-03-10 09:30",
      end: "2024-03-10 11:00",
      description: "This is event 5 description.",
      location: "Hyderabad, India"
    },
    {
      id: 6,
      title: "Event 6",
      start: "2024-03-14 14:00",
      end: "2024-03-14 16:00",
      description: "This is event 6 description.",
      location: "Kolkata, India"
    },
    {
      id: 7,
      title: "Event 7",
      start: "2024-03-16 11:00",
      end: "2024-03-16 12:30",
      description: "This is event 7 description.",
      location: "Pune, India"
    },
    {
      id: 8,
      title: "Event 8",
      start: "2024-03-18 08:30",
      end: "2024-03-18 10:00",
      description: "This is event 8 description.",
      location: "Ahmedabad, India"
    },
    {
      id: 9,
      title: "Event 9",
      start: "2024-03-21 13:00",
      end: "2024-03-21 14:30",
      description: "This is event 9 description.",
      location: "Jaipur, India"
    },
    {
      id: 10,
      title: "Event 10",
      start: "2024-03-24 10:30",
      end: "2024-03-24 12:00",
      description: "This is event 10 description.",
      location: "Lucknow, India"
    },
    {
      id: 11,
      title: "Event 11",
      start: "2024-03-27 16:00",
      end: "2024-03-27 18:00",
      description: "This is event 11 description.",
      location: "Patna, India"
    },
    {
      id: 12,
      title: "Event 12",
      start: "2024-03-29 09:00",
      end: "2024-03-29 10:30",
      description: "This is event 12 description.",
      location: "Gurgaon, India"
    },
    {
      id: 13,
      title: "Event 13",
      start: "2024-03-03 14:00",
      end: "2024-03-03 15:30",
      description: "This is event 13 description.",
      location: "Noida, India"
    },
    {
      id: 14,
      title: "Event 14",
      start: "2024-03-06 11:00",
      end: "2024-03-06 13:00",
      description: "This is event 14 description.",
      location: "Ghaziabad, India"
    },
    {
      id: 15,
      title: "Event 15",
      start: "2024-03-09 10:30",
      end: "2024-03-09 12:00",
      description: "This is event 15 description.",
      location: "Faridabad, India"
    },
    {
      id: 16,
      title: "Event 16",
      start: "2024-03-12 09:00",
      end: "2024-03-12 10:30",
      description: "This is event 16 description.",
      location: "Chandigarh, India"
    },
    {
      id: 17,
      title: "Event 17",
      start: "2024-03-15 14:00",
      end: "2024-03-15 16:00",
      description: "This is event 17 description.",
      location: "Indore, India"
    },
    {
      id: 18,
      title: "Event 18",
      start: "2024-03-17 12:30",
      end: "2024-03-17 14:00",
      description: "This is event 18 description.",
      location: "Nagpur, India"
    },
    {
      id: 19,
      title: "Event 19",
      start: "2024-03-21 09:00",
      end: "2024-03-21 10:30",
      description: "This is event 19 description.",
      location: "Kanpur, India"
    },
    {
      id: 20,
      title: "Event 20",
      start: "2024-03-23 13:00",
      end: "2024-03-23 14:30",
      description: "This is event 20 description.",
      location: "Thane, India"
    },
    {
      id: 21,
      title: "Event 21",
      start: "2024-03-26 11:30",
      end: "2024-03-26 13:00",
      description: "This is event 21 description.",
      location: "Bhopal, India"
    },
    {
      id: 22,
      title: "Event 22",
      start: "2024-03-28 15:00",
      end: "2024-03-28 16:30",
      description: "This is event 22 description.",
      location: "Visakhapatnam, India"
    },
    {
      id: 23,
      title: "Event 23",
      start: "2024-03-01 09:00",
      end: "2024-03-01 10:30",
      description: "This is event 23 description.",
      location: "Surat, India"
    },
    {
      id: 24,
      title: "Event 24",
      start: "2024-03-05 14:00",
      end: "2024-03-05 15:30",
      description: "This is event 24 description.",
      location: "Patiala, India"
    },
    {
      id: 25,
      title: "Event 25",
      start: "2024-03-07 11:00",
      end: "2024-03-07 12:30",
      description: "This is event 25 description.",
      location: "Amritsar, India"
    },
  ],
  calendars: {
    work: {
      colorName: 'work',
      lightColors: {
        container: '#fff',
        onContainer: '#000',
        main: '#fff',
      },
      darkColors: {
        container: '#000',
        onContainer: '#fff',
        main: '#000',
      },
    }
  }
})

const eventTitle = ref('');
const eventStart = ref('');
const eventEnd = ref('');
const eventDescription = ref('');
const eventLocation = ref('');
const eventId = ref(calendarApp.events.getAll().length);

const addEvent = () => {
  let data = {
    id: eventId.value + 1,
    title: eventTitle.value,
    start: eventStart.value,
    end: eventEnd.value,
    description: eventDescription.value,
    location: eventLocation.value
  }
  console.log(data)
  calendarApp.events.add(data);
  console.log(calendarApp.events.getAll())
  eventTitle.value = '';
  eventStart.value = '';
  eventEnd.value = '';
  eventDescription.value = '';
  eventLocation.value = '';
  eventId.value = calendarApp.events.getAll().length
};

const deleteEvent = (id) => {
  calendarApp.events.remove(id);
};

const updateEvent = (id, updatedEvent) => {
  calendarApp.events.update(id, updatedEvent);
};
</script>

<template>
  <div class="h-full overflow-hidden">
    <div>
      <div data-modal-target="crud-modal" data-modal-toggle="crud-modal"
        class="flex items-center justify-center text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-100 font-medium rounded-lg py-2.5 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700 text-center cursor-pointer"
        type="button">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
          class="w-5 h-5">
          <path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m7.5-7.5h-15" />
        </svg>
        Add Event
      </div>
    </div>
    <ClientOnly>
      <ScheduleXCalendar :calendar-app="calendarApp" />
    </ClientOnly>

    <div id="crud-modal" tabindex="-1" aria-hidden="true"
      class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full">
      <div class="relative p-4 w-full max-w-md max-h-full">
        <div class="relative bg-white rounded-lg shadow dark:bg-gray-700">
          <div class="flex items-center justify-between p-4 md:p-5 border-b rounded-t dark:border-gray-600">
            <h3 class="text-lg font-semibold text-gray-900 dark:text-white">
              Add New Event
            </h3>
            <button type="button"
              class="text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm w-8 h-8 ms-auto inline-flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white"
              data-modal-toggle="crud-modal">
              <svg class="w-3 h-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
                viewBox="0 0 14 14">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6" />
              </svg>
              <span class="sr-only">Close modal</span>
            </button>
          </div>
          <form class="p-4 md:p-5">
            <div class="grid gap-4 mb-4 grid-cols-2">
              <div class="col-span-2">
                <label for=title class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Event
                  Title</label>
                <input v-model="eventTitle" type="text" name=title id=title
                  class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
                  placeholder="Type your title" required="">
              </div>
              <div class="col-span-2">
                <label for=location
                  class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Location</label>
                <input v-model="eventLocation" type="text" name=location id=location
                  class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
                  placeholder="Type your location" required="">
              </div>
              <div class="col-span-2 sm:col-span-1">
                <label for=start class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Start</label>
                <input v-model="eventStart" type="datetime-local" name=start id=start
                  class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
                  placeholder="$2999" required="">
              </div>
              <div class="col-span-2 sm:col-span-1">
                <label for=end class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">End</label>
                <input v-model="eventEnd" type="datetime-local" name=end id=end
                  class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-600 focus:border-primary-600 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
                  placeholder="$2999" required="">
              </div>
              <div class="col-span-2">
                <label for=description
                  class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Description</label>
                <textarea v-model="eventDescription" id=description rows="4"
                  class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                  placeholder="Write product description here"></textarea>
              </div>
            </div>
            <button @click="addEvent" type="button"
              class="text-white inline-flex items-center bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
              Submit
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.sx-vue-calendar-wrapper {
  height: 700px;
  max-height: 90vh;
  width: 100%;
}
</style>


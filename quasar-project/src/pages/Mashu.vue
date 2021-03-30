<template>
  <div>
    <h3>Hello from Mashu</h3>
    <q-banner v-if="isClicked" class="bg-primary text-white">
      Unfortunately, the credit card did not go through, please try again.
      <template v-slot:action>
        <q-btn flat color="white" label="Dismiss" v-on:click="close" />
        <q-btn flat color="white" label="Update Credit Card" />
      </template>
    </q-banner>
    <q-btn
      v-on:click="clicked"
      color="primary"
      label="Click me"
      class="button"
    />
    <div class="q-pa-md q-gutter-md">
      <div>
        <q-chip icon="event">Add to calendar</q-chip>
        <q-chip icon="bookmark">Bookmark</q-chip>
        <q-chip icon="alarm" label="Set alarm" />
        <q-chip class="glossy" icon="directions">Get directions</q-chip>
      </div>
      <div>
        <q-chip color="primary" text-color="white" icon="event">
          Add to calendar
        </q-chip>
        <q-chip color="teal" text-color="white" icon="bookmark">
          Bookmark
        </q-chip>
        <q-chip
          class="glossy"
          color="orange"
          text-color="white"
          icon-right="star"
        >
          Star
        </q-chip>
        <q-chip color="red" text-color="white" icon="alarm" label="Set alarm" />
        <q-chip color="deep-orange" text-color="white" icon="directions">
          Get directions
        </q-chip>
        <q-chip>
          <q-avatar icon="bookmark" color="red" text-color="white" />
          Bookmark
        </q-chip>
        <q-chip>
          <q-avatar color="red" text-color="white">50</q-avatar>
          Emails
        </q-chip>
        <q-chip>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/avatar5.jpg" />
          </q-avatar>
          John
        </q-chip>
      </div>
    </div>
    <div class="q-pa-md">
      <q-carousel
        v-model="slide"
        vertical
        transition-prev="slide-down"
        transition-next="slide-up"
        swipeable
        animated
        control-color="white"
        navigation-icon="radio_button_unchecked"
        navigation
        padding
        arrows
        height="300px"
        class="bg-purple text-white shadow-1 rounded-borders"
      >
        <q-carousel-slide name="style" class="column no-wrap flex-center">
          <q-icon name="style" size="56px" />
          <div class="q-mt-md text-center">
            {{ lorem }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="tv" class="column no-wrap flex-center">
          <q-icon name="live_tv" size="56px" />
          <div class="q-mt-md text-center">
            {{ lorem }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="layers" class="column no-wrap flex-center">
          <q-icon name="layers" size="56px" />
          <div class="q-mt-md text-center">
            {{ lorem }}
          </div>
        </q-carousel-slide>
        <q-carousel-slide name="map" class="column no-wrap flex-center">
          <q-icon name="terrain" size="56px" />
          <div class="q-mt-md text-center">
            {{ lorem }}
          </div>
        </q-carousel-slide>
      </q-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      isClicked: false,
      slide: 'style',
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    };
  },
  methods: {
    clicked() {
      this.isClicked = true;
    },
    close() {
      this.isClicked = false;
    }
  }
};
</script>

<style></style>

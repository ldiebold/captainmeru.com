<script lang="ts" setup>
import LukePhoto from 'assets/profile-photos/luke.jpg'
import RandyPhoto from 'assets/profile-photos/randy-joe.jpg'
import ShannenPhoto from 'assets/profile-photos/shannen.jpg'

const testimonials = [
  {
    author: {
      name: 'Luke Diebold',
      profilePhoto: LukePhoto,
    },
    body: "We hired Captain Meru for a short trip to the city. Next thing we know, we're seeing parts of Vanuatu only the locals get to see. Best. Holiday. EVER!",
  },
  {
    author: {
      name: 'Randy Joe',
      profilePhoto: RandyPhoto,
    },
    body: 'We thought we knew where we wanted to go but had no idea! Captain Meru told us all the best spots and we had a great chat along the way. Highly recommend.',
  },
  {
    author: {
      name: 'Shannen Higginson',
      profilePhoto: ShannenPhoto,
    },
    body: 'I experienced secret parts of the island I never would have known existed. Now I want to live here!',
  },
]
</script>

<template>
  <div class="column justify-around">
    <div class="row justify-around items-start q-col-gutter-xl">
      <h2 class="full-width text-center q-mb-none">
        We Love Captain Meru!
      </h2>
      <div
        v-for="testimonial in testimonials"
        :key="testimonial.body"
        class="col-xs-12 col-md-6 col-lg-4 row justify-center"
      >
        <q-card
          style="max-width: 400px"
          class="text-center"
        >
          <q-img
            :ratio="1"
            :src="testimonial.author.profilePhoto"
          />
          <div class=" q-my-md text-3xl text-grey-7">
            {{ testimonial.author.name }}
          </div>
          <q-separator />
          <q-card-section class="q-my-md text-2xl text-grey-9">
            {{ testimonial.body }}
          </q-card-section>
        </q-card>
      </div>
    </div>
  </div>
</template>

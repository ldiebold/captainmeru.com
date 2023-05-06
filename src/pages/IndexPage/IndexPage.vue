<script setup lang="ts">
import FeatureSection from 'src/layouts/MainLayout/FeatureSection.vue'
import QuoteSection from 'src/layouts/MainLayout/QuoteSection.vue'
import UnderwaterPostFeature from 'assets/feature-photos/underwaterpost.jpg'
import SnorkelingFeature from 'assets/feature-photos/snorkeling.jpg'
import FireShowFeature from 'assets/feature-photos/fire-show.jpg'
import { mdiArrowDown, mdiPhone } from '@quasar/extras/mdi-v7'
import TestimonialsSection from 'src/layouts/MainLayout/TestimonialsSection.vue'

const phoneNumber = '6711 473'
</script>

<template>
  <q-page
    class="row justify-center"
  >
    <div class="col-xs-11 col-lg-10 q-mb-xl">
      <div class="text-center q-mt-lg">
        <h1 class="q-my-none text-2.8em leading-1.4em lg:text-6em lg:leading-1.2em">
          <strong>Captain Meru</strong>: The Ultimate Vanuatu Skipper, Tour Guide, And Friend
        </h1>
        <h2 class="q-my-none text-1.8em leading-1.2em lg:text-2.4em lg:leading-1.7em q-mt-none text-grey-8">
          "I Promise, You've <strong>NEVER</strong> Been On An <strong>Adventure</strong> Like This!!!"
        </h2>
      </div>
      <div class="row q-mt-md q-col-gutter-xl justify-center">
        <div class="col-xs-11 col-lg-7">
          <q-video
            src="https://www.youtube.com/embed/cLjtu71qHbg"
            :ratio="16/9"
            class="full-width bg-blue-2"
          />
        </div>
        <div class="col-xs-11 col-lg-5 text-weight-light q-gutter-y-md text-2.1em">
          <li>Experience <strong>UNREAL</strong> marine life, snorkling in crystal waters so clear... you won't miss a thing!</li>
          <li>Watch Vanuatu's <strong>INSANELY</strong> talented <strong class="text-red-8">FIRE spinners</strong> in a show you <strong>WILL NOT</strong> want to miss AND...</li>
          <li>Be <strong>in the know</strong> about Vanuatu's latest hapennings from a local of almost 50 years!</li>
          <li>EXPERIENCE Vanuatu's <strong>culture and secrets</strong>. There's more to these beautiful islands than meets the eye...</li>
        </div>
      </div>
    </div>

    <div class="col-12 row justify-center q-mb-xl">
      <q-btn
        size="xl"
        color="secondary"
        padding="32px 66px"
        type="a"
        :href="`tel:${phoneNumber}`"
      >
        <div class="column">
          <div>Book Now</div>
          <div>
            <q-icon
              class="q-mr-sm"
              :name="mdiPhone"
            />{{ phoneNumber }}
          </div>
        </div>
      </q-btn>
    </div>

    <QuoteSection class="h-88vh" />

    <div class="col-xs-11 col-lg-10 q-mb-xl">
      <div class="min-h-90vh">
        <FeatureSection
          title="The BEST Snorkeling In Vanuatu..."
          :img="SnorkelingFeature"
          body="The <strong>sea life</strong> in Vanuatu is mind blowing BUT, you need to know the right spots. Captain Meru knows all the best places for snorkeling, free diving and scuba diving <strong>AND he'll take you there!</strong>"
          class="my-5em"
        />
      </div>

      <div class="min-h-90vh">
        <FeatureSection
          title="Fire. A Night You'll Never Forget!"
          :img="FireShowFeature"
          body="Captain Meru insisted we see the <strong>fire show</strong> (which is free), so we decided to check it out. What an experience! We could literally <strong>feel the heat</strong>, and the performers were very kind and friendly after the show. They even <strong>let us spin the fire</strong>!"
          class="my-5em reverse"
        />
      </div>

      <div class="min-h-90vh">
        <FeatureSection
          title="Ever Posted A Letter From An Under Water Post Office!?"
          :img="UnderwaterPostFeature"
          body="This is not just for show, you can literally post a letter in the <strong>worlds first underwater post office!</strong> How? They give you a water proof card, you swim out to the platoon, dive under, and deliver the postcard into an underwater post office! <strong>It's a wild experience!</strong>...<br> <br> Oh, and the snorkeling on 'Hide Away Island' kept us <strong>engaged for HOURS!</strong>"
          class="my-5em"
        />
      </div>

      <TestimonialsSection class="min-h-100vh" />
    </div>
    <div class="text-h4 text-center q-my-none text-white bg-primary py-8rem px-10 lg:px-100 flex flex-center">
      <div>
        Click Below To Book Now! Captain Meru books out fast and trust us, he'll make your holiday one to remember!
      </div>
      <q-btn
        class="q-mt-lg"
        size="xl"
        color="secondary"
        padding="32px 66px"
        type="a"
        :href="`tel:${phoneNumber}`"
      >
        <div class="column">
          <div>Book Now</div>
          <div>
            <q-icon
              class="q-mr-sm"
              :name="mdiPhone"
            />{{ phoneNumber }}
          </div>
        </div>
      </q-btn>
    </div>

    <q-page-sticky :offset="[18,18]">
      <q-btn
        fab
        color="secondary"
        :icon="mdiPhone"
        type="a"
        :href="`tel:${phoneNumber}`"
      />
    </q-page-sticky>
  </q-page>
</template>

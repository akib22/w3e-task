<template>
  <q-page class="p-relative bg-footer">
    <image-slider />

    <div class="q-px-md q-pb-sm">
      <h4 class="q-my-xs text-indigo-10">heading for app property.</h4>
      <q-breadcrumbs class="text-grey">
        <template v-slot:separator>
          <q-icon size="1.5em" name="chevron_right" color="primary" />
        </template>

        <q-breadcrumbs-el to="/" label="Home" />
        <q-breadcrumbs-el to="/properties" label="Properties" />
        <q-breadcrumbs-el label="Property Title" />
      </q-breadcrumbs>
      <div class="rental-info q-py-md">
        <p class="text-subtitle2">Night rates from:</p>
        <div class="row justify-between">
          <p class="col-6 text-h6 text-weight-medium">CAD $26,290</p>
          <p class="col-6 text-h6 text-weight-medium">Min 2 Night Stay</p>
        </div>
      </div>
      <div class="propety-info">
        <div class="row justify-between">
          <div class="flex col-6">
            <q-icon color="indigo-10 q-mr-sm" name="people" size="22px" />
            <p class="text-subtitle2 text-grey">6 Guests</p>
          </div>
          <div class="flex col-6">
            <q-icon color="indigo-10 q-mr-sm" name="hotel" size="22px" />
            <p class="text-subtitle2 text-grey">4 Bedrooms</p>
          </div>
        </div>
        <div class="row justify-between">
          <div class="flex col-6">
            <q-icon color="indigo-10 q-mr-sm" name="bathtub" size="22px" />
            <p class="text-subtitle2 text-grey">2 Bathrooms</p>
          </div>
          <div class="flex col-6">
            <q-icon color="indigo-10 q-mr-sm" name="pets" size="22px" />
            <p class="text-subtitle2 text-grey">Pet friendly</p>
          </div>
        </div>
      </div>
      <q-btn
        flat
        rounded
        label="Check Availablity"
        class="full-width bg-green-6 text-white text-h5 text-weight-bolder q-my-md"
      />
      <q-tabs
        v-model="tab"
        class="text-grey"
        active-color="primary"
        indicator-color="none"
        align="justify"
        narrow-indicator
      >
        <q-tab name="overview" label="Overview" />
        <q-tab name="map" label="Map" />
        <q-tab name="amenities" label="Amenities" />
        <q-tab name="faqs" label="FAQs" />
      </q-tabs>
      <q-tab-panels v-model="tab" animated class="bg-footer">
        <q-tab-panel class="text-body1" name="overview">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem ipsum
          dolor sit amet consectetur adipisicing elit. Lorem ipsum dolor sit
          amet consectetur adipisicing elit.
        </q-tab-panel>

        <q-tab-panel class="text-body1" name="map">
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>

        <q-tab-panel class="text-body1" name="amenities">
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
        <q-tab-panel class="text-body1" name="faqs">
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
      </q-tab-panels>
    </div>
    <!-- <div class="p-absolute suggestion bg-footer">
      <suggestion />
    </div> -->
  </q-page>
</template>

<script>
import ImageSlider from "src/components/ImageSlider.vue";

export default {
  components: { ImageSlider },
  data() {
    return {
      tab: "overview"
    };
  }
};
</script>

<style scoped>
.suggestion{
  top: 100%;
  z-index: 99;
}
</style>

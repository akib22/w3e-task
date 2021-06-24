<template>
  <q-card class="my-card q-my-sm p-relative">
    <q-card-section horizontal>
      <q-img class="col-5" src="https://cdn.quasar.dev/img/parallax1.jpg" />

      <q-card-section>
        <q-breadcrumbs active-color="grey" class="text-grey" gutter="xs">
          <q-breadcrumbs-el label="House" />
          <q-breadcrumbs-el label="Sleep 1" />
          <q-breadcrumbs-el label="Bed 2" />
        </q-breadcrumbs>
        <p class="text-subtitle1 text-weight-medium">
          Hayatt Regency Coral
        </p>
        <div class="flex">
          <q-rating
            disable
            :value="4"
            size="1em"
            color="green-5"
            icon="star_border"
            icon-selected="star"
            class="q-mr-sm"
          />
          <span class="text-subtitle1">4 (56 reviews)</span>
        </div>
        <q-breadcrumbs active-color="grey" class="text-grey" gutter="xs">
          <template v-slot:separator>
            <q-icon size="0.8em" name="fiber_manual_record" color="grey" />
          </template>
          <q-breadcrumbs-el label="Wifi" />
          <q-breadcrumbs-el label="Laundry" />
          <q-breadcrumbs-el label="Pool" />
        </q-breadcrumbs>
        <div class="flex">
          <span class="text-subtilte1 text-weight-bold text-indigo-10"
            >Booking.com</span
          >
          <div>
            <div class="q-mb-xs">Nightly rates from:</div>
            <div class="q-pa-sm bg-green-6 text-white rounded-borders">
              <div class="flex items-baseline">
                <span class="q-mr-xs text-weight-medium">CAD</span>
                <span class="text-h6 text-weight-medium">$26,290</span>
              </div>
            </div>
          </div>
        </div>
      </q-card-section>
    </q-card-section>
    <div class="p-absolute like">
      <like />
    </div>
    <div v-if="hotDeal" class="p-absolute badge">
      <q-chip color="white">Hot deal</q-chip>
    </div>
  </q-card>
</template>

<script>
import Like from "./Like.vue";

export default {
  name: "Card",
  props: ["hotDeal"],
  components: { Like }
};
</script>

<style scoped>
.like {
  left: 5px;
  bottom: 5px;
}
.badge {
  left: 0px;
  top: 10px;
}
</style>

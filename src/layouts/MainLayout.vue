<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-indigo-10">
      <q-toolbar>
        <q-btn round flat icon="apps" />
        <q-toolbar-title>
          AirBNB
        </q-toolbar-title>
      
        <Search />
        <q-btn
          flat
          dense
          round
          :icon="icon"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />
      </q-toolbar>
    </q-header>

    <q-drawer
      side="right"
      v-model="leftDrawerOpen"
      bordered
      overlay
      content-class="bg-grey-1"
    >
      <q-list>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
    <Footer />
  </q-layout>
</template>

<script>
import Search from "components/Search.vue";
import Footer from "components/Footer.vue";
import EssentialLink from "src/components/Drawer.vue";

const linksData = [
  {
    title: "Home",
    icon: "home",
    link: "/"
  },
  {
    title: "Properties",
    icon: "code",
    link: "/properties"
  },
  {
    title: "Forum",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev"
  },
  {
    title: "Twitter",
    caption: "@quasarframework",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev"
  },
  {
    title: "Facebook",
    caption: "@QuasarFramework",
    icon: "public",
    link: "https://facebook.quasar.dev"
  },
];

export default {
  name: "MainLayout",
  components: { EssentialLink, Search, Footer },
  data() {
    return {
      leftDrawerOpen: false,
      essentialLinks: linksData
    };
  },
  computed: {
    icon: function() {
      return this.leftDrawerOpen ? "close" : "menu";
    }
  }
};
</script>

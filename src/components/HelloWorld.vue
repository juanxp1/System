<template>
  <v-container fluid>
    <v-row>
      <v-col>
        <v-window v-model="store.tab">
          <v-window-item v-for="n in 6" :key="n" :value="n">
            <v-container fluid>
              <v-row>
                <v-col v-for="i in 1" :key="i">
                  <component :is="getComponentForTab(store.tab)"></component>
                </v-col>
              </v-row>
            </v-container>
          </v-window-item>
        </v-window>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { useAppStore } from '@/store/app';
import About from './About.vue';
import Services from './Services.vue';
import Products from './Products.vue';
import Employment from './Employment.vue';
import FAQ from './Faq.vue';
import Contacts from './Contacts.vue';

const store = useAppStore();

const getComponentForTab = (tab) => {
  switch (tab) {
    case 1:
      return About;
    case 2:
      return Services;
    case 3:
      return Products;
    case 4:
      return Employment;
    case 5:
      return FAQ;
    case 6:
      return Contacts;
    default:
      return About;
  }
};
</script>

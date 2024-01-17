<template>
  <v-sheet>
    <div class="banner">
      <div class="d-flex align-center justify-content-between p-5 container log-text">
        <img :src="logo" alt="Logo" class="logo">
        <v-divider class="custom-divider" :thickness="1" color="white" vertical></v-divider>
        <div>
          <p>Soluciones para la Seguridad y Comunicaciones</p>
          <Icons />
        </div>
      </div>
      <div class="d-flex justify-content-center">
        <v-card class="menu" color="yellow-darken-3">
          <v-tabs v-model="store.tab" color="grey-lighten-5" align-tabs="center">
            <v-tab :value="1">About</v-tab>
            <v-divider :thickness="2" color="black" vertical></v-divider>
            <v-tab :value="2">Services</v-tab>
            <v-divider :thickness="2" color="black" vertical></v-divider>
            <v-tab :value="3">Products</v-tab>
            <v-divider :thickness="2" color="black" vertical></v-divider>
            <v-tab :value="4">Employment</v-tab>
            <v-divider :thickness="2" color="black" vertical></v-divider>
            <v-tab :value="5">FAQ</v-tab>
            <v-divider :thickness="2" color="black" vertical></v-divider>
            <v-tab :value="6">Contacts</v-tab>
          </v-tabs>
        </v-card>
      </div>
    </div>
  </v-sheet>
</template>

<script setup>
import logo from '@/assets/logo.png'
import Icons from '@/components/Icons.vue';
import { useAppStore } from '@/store/app';
const store = useAppStore()
</script>

<style scoped>
.custom-divider {
  height: 50px;
}

.menu {
  width: 55%;
  align-items: center;
  border-radius: 15px;
  height: 60px;
  justify-content: center;
  display: flex;
  margin-top: 40px;
}

.menu .v-tab {
  text-transform: none;
  font-size: 19px;
  font-weight: 500;
  font-family: Arial, Helvetica, sans-serif;
}

.logo {
  transition: transform 0.6s ease-in-out;
  border-radius: 20px;
  padding: 10px;
  padding-left: 25px;
  padding-right: 25px;
}

.logo:hover {
  border-radius: 20px;
}

p {
  font-style: italic;
  cursor: pointer;
  font-family: 'Courier New', Courier, monospace;
  color: rgba(241, 241, 241, 0.3);
}


.banner {
  background-image: url('@/assets/bgg.png');
  height: 18rem;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

@media (max-width:768px) {
  .logo {
    width: 100%;
  }

  .banner {
    height: auto;
    padding: 0px;
    margin: 0px;
  }

  .log-text {
    flex-direction: column;
    justify-content: center;
  }

  p {
    text-align: center;
  }

  .menu {
    width: 100%;
    border-radius: 0px;
  }
}
</style>

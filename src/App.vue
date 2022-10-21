<script setup>
  import { ref } from "vue";
  const displayModal = ref(false);
</script>

<template>
  <img alt="Logo" class="logo" src="https://primefaces.org/primevue/demo/images/primevue-logo-dark.svg" v-tooltip="'Logo'" style="position:relative; z-index:2; margin-bottom:2rem;"/>
  <Button label="Show" icon="pi pi-external-link" @click="displayModal = true;" style="position:relative; z-index:2; margin-bottom:2rem;" />
  <p style="position:relative; z-index:2;">Click the button above BEFORE hovering over the PrimeVue icon, then try clicking the buton above AFTER hovering over the PrimeVue icon.</p>
  <Dialog header="Header" v-model:visible="displayModal" :style="{width: '50vw'}" :modal="true">
    <p class="m-0">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </Dialog>
</template>

<style>
  #app {
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
</style>
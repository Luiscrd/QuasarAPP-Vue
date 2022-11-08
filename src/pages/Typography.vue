<template>
  <q-page class="q-pa-md">
    <span class="text-h3">Typography</span>

    <q-separator spaced />
    <template class="flex column q-pa-md">
      <span class="text-h1">Hedline 1</span>
      <span class="text-h2">Hedline 2</span>
      <span class="text-h3">Hedline 3</span>
      <span class="text-h4">Hedline 4</span>
      <span class="text-h5">Hedline 5</span>
      <span class="text-h6">Hedline 6</span>

      <q-separator />

      <span class="text-subtitle1">Subtitle 1</span>
      <span class="text-subtitle2">Subtitle 2</span>

      <q-separator />

      <p class="text-subtitle1">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veniam,
        deleniti! Ut architecto velit optio consectetur asperiores omnis
        aspernatur porro expedita!
      </p>
      <p class="text-subtitle2">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veniam,
        deleniti! Ut architecto velit optio consectetur asperiores omnis
        aspernatur porro expedita!
      </p>

      <q-separator />

      <span class="text-weight-thin"
        >Lorem Ipsum is simply dummy text of the printing and typesetting
        industry.</span
      >
      <span class="text-weight-light"
        >Lorem Ipsum is simply dummy text of the printing and typesetting
        industry.</span
      >
      <span class="text-weight-regular"
        >Lorem Ipsum is simply dummy text of the printing and typesetting
        industry.</span
      >
      <span class="text-weight-medium"
        >Lorem Ipsum is simply dummy text of the printing and typesetting
        industry.</span
      >
      <span class="text-weight-bold"
        >Lorem Ipsum is simply dummy text of the printing and typesetting
        industry.</span
      >
      <span class="text-weight-bolder"
        >Lorem Ipsum is simply dummy text of the printing and typesetting
        industry.</span
      >

      <q-separator />

      <q-btn
        color="primary"
        :label="sideMenuOpen ? 'Cerrar Menú' : 'Abrir Menú'"
        class="q-mt-md"
        @click="toggleSideMenu"
      />
    </template>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import useUI from "../composables/useUI";

export default defineComponent({
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Typography",
  setup() {
    const { sideMenuOpen, toggleSideMenu } = useUI();

    return {
      sideMenuOpen,
      toggleSideMenu,
    };
  },
});
</script>

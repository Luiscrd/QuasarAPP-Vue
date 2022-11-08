<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <q-page class="q-pa-md">
    <span class="text-h3">Flex</span>

    <q-separator spaced />
    <span class="text-h4">Usando row con col sin definir</span>
    <div class="row q-mb-md q-mt-md">
      <div class="col bg-primary text-center q-py-md">col</div>
      <div class="col bg-secondary text-center q-py-md">col</div>
      <div class="col bg-accent text-center q-py-md">col</div>
    </div>

    <span class="text-h4">Usando row con col definiendo tamaño</span>
    <div class="row q-mb-md">
      <div class="col bg-primary text-center q-py-md">col</div>
      <div class="col-6 bg-secondary text-center q-py-md">col-6</div>
      <div class="col-5 bg-accent text-center q-py-md">col-5</div>
    </div>

    <q-separator spaced />

    <div class="row q-mb-md q-mt-md justify-start">
      <div class="col-4 bg-primary text-center q-py-md"></div>
      <div class="col-4 bg-secondary text-center q-py-md"></div>
    </div>

    <div class="row q-mb-md justify-center">
      <div class="col-4 bg-primary text-center q-py-md"></div>
      <div class="col-4 bg-secondary text-center q-py-md"></div>
    </div>

    <div class="row q-mb-md justify-end">
      <div class="col-4 bg-primary text-center q-py-md"></div>
      <div class="col-4 bg-secondary text-center q-py-md"></div>
    </div>

    <div class="row q-mb-md justify-between">
      <div class="col-4 bg-primary text-center q-py-md"></div>
      <div class="col-4 bg-secondary text-center q-py-md"></div>
    </div>

    <q-separator spaced />

    <div class="row q-mb-md q-mt-md justify-between">
      <div
        class="col-12 col-sm-5 col-md-4 bg-primary text-center q-py-md"
      ></div>
      <div
        class="col-12 col-sm-5 col-md-4 bg-secondary text-center q-py-md"
      ></div>
    </div>

    <q-separator spaced />

    <div class="row q-mt-md">
      <div class="square-box bg-primary text-center q-py-md"></div>
      <div class="square-box bg-secondary text-center q-py-md"></div>
      <div class="square-box bg-accent text-center q-py-md"></div>
    </div>

    <div class="row q-mt-md justify-between">
      <div class="square-box bg-primary text-center q-py-md"></div>
      <div class="square-box bg-secondary text-center q-py-md"></div>
      <div class="square-box bg-accent text-center q-py-md"></div>
    </div>

    <div class="row q-mt-md justify-around">
      <div class="square-box bg-primary text-center q-py-md"></div>
      <div class="square-box bg-secondary text-center q-py-md"></div>
      <div class="square-box bg-accent text-center q-py-md"></div>
    </div>

    <q-separator spaced />

    <div class="column q-mt-md items-start bg-dark">
      <div class="square-box bg-primary text-center q-py-md"></div>
      <div class="square-box bg-secondary text-center q-py-md"></div>
      <div class="square-box bg-accent text-center q-py-md"></div>
    </div>

    <div class="column q-mt-md items-center bg-dark">
      <div class="square-box bg-primary text-center q-py-md"></div>
      <div class="square-box bg-secondary text-center q-py-md"></div>
      <div class="square-box bg-accent text-center q-py-md"></div>
    </div>

    <div class="column q-mt-md items-end bg-dark">
      <div class="square-box bg-primary text-center q-py-md"></div>
      <div class="square-box bg-secondary text-center q-py-md"></div>
      <div class="square-box bg-accent text-center q-py-md"></div>
    </div>

    <div
      class="column custom-height q-mt-md items-center justify-center bg-dark"
    >
      <div class="square-box bg-primary text-center q-py-md"></div>
      <div class="square-box bg-secondary text-center q-py-md"></div>
      <div class="square-box bg-accent text-center q-py-md"></div>
    </div>

    <div
      class="column custom-height q-mt-md items-center justify-between bg-dark"
    >
      <div class="square-box bg-primary text-center q-py-md"></div>
      <div class="square-box bg-secondary text-center q-py-md"></div>
      <div class="square-box bg-accent text-center q-py-md"></div>
    </div>

    <div
      class="column custom-height q-mt-md items-center justify-between bg-dark"
    >
      <div class="square-box self-start bg-accent text-center q-py-md"></div>
      <div class="square-box self-center bg-primary text-center q-py-md"></div>
      <div class="square-box self-end bg-secondary text-center q-py-md"></div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Flex",
});
</script>

<style scoped>
.col,
.col-1,
.col-4,
.col-6,
.col-12 {
  height: 50px;
}

.square-box {
  width: 50px;
  height: 50px;
}

.custom-height {
  height: 250px;
}
</style>
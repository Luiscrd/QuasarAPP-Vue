<template>
  <q-page class="q-pa-md">
    <span class="text-h3">Froms</span>

    <q-separator spaced />

    <div class="row q-pa-md">
      <q-form
        @submit="onSubmit"
        @reset="onReset"
        class="q-gutter-xs col-xs-12 col-sm-6 col-md-6 col-6"
      >
        <q-input
          filled
          v-model="userFrom.email"
          label="Correo electronico *"
          type="email"
          lazy-rules
          :rules="[
            (val) =>
              (val && val.length > 0) || 'Introduce un correo electronicco',
            isValidEmail,
          ]"
        />

        <q-input
          filled
          type="password"
          v-model="userFrom.password"
          label="Introduce contraseña *"
          lazy-rules
          :rules="[
            (val) => (val !== null && val !== '') || 'Introduce contraeña',
          ]"
        />

        <q-input
          filled
          type="password"
          v-model="userFrom.password2"
          label="Repite contraseña *"
          lazy-rules
          :rules="[
            (val) => (val !== null && val !== '') || 'Introduce contraeña',
            isSamePassword,
          ]"
        />

        <q-toggle
          v-model="userFrom.conditions"
          label="Aceptar terminos y condiciones de uso"
          :style="
            userFrom.errorInConditions && !userFrom.conditions
              ? 'color: red'
              : ''
          "
        />

        <div class="row justify-end">
          <q-btn
            label="Reset"
            type="reset"
            color="primary"
            flat
            class="q-ml-sm"
          />
          <q-btn
            unelevated
            label="Submit"
            type="submit"
            :color="
              userFrom.errorInConditions && !userFrom.conditions
                ? 'red'
                : 'primary'
            "
          />
        </div>
      </q-form>
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";
import { useQuasar } from "quasar";

export default defineComponent({
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Forms",
  setup() {
    const $q = useQuasar();

    const userFrom = ref({
      email: "",
      password: "",
      password2: "",
      conditions: false,
      errorInConditions: false,
    });

    return {
      userFrom,
      onSubmit() {
        userFrom.value.errorInConditions = false;

        if (!userFrom.value.conditions) {
          userFrom.value.errorInConditions = true;
          $q.notify({
            type: "negative",
            message: "Debe de aceptar los terminos y condiciones de uso",
          });
        }
      },
      onReset() {
        userFrom.value = {
          email: "",
          password: "",
          password2: "",
          conditions: false,
          errorInConditions: false,
        };
      },
      isValidEmail(val) {
        const emailPattern =
          /^(?=[a-zA-Z0-9@._%+-]{6,254}$)[a-zA-Z0-9._%+-]{1,64}@(?:[a-zA-Z0-9-]{1,63}\.){1,8}[a-zA-Z]{2,63}$/;
        return emailPattern.test(val) || "El correo no es válido";
      },
      isSamePassword(val) {
        return (
          val === userFrom.value.password || "Las contraseñas no son iguales"
        );
      },
    };
  },
});
</script>

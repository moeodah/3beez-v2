<template>
  <q-page class="flex-center">
        <q-card class="q-pa-md">
        <q-tabs
          dense
          class="text-grey"
          active-color="primary"
          indicator-color="primary"
          align="justify"
          narrow-indicator
        >
          <q-tab name="register" label="Register" />
        </q-tabs>

        <q-separator />



          <q-tab-panel name="register">
            <login-register :tab="tab"/>
          </q-tab-panel>
      </q-card>
  </q-page>
</template>

<script>
import { ref } from 'vue'

export default {
  data () {
    return {
      tab: ref('login')
    }
  },
  components: {
    'login-register': require('components/LoginRegister.vue').default
  }
}
</script>

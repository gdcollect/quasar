<template>
  <div class="q-pa-md">
    <div class="q-gutter-md column" style="max-width: 300px">
      <q-input rounded filled v-model="text">
        <template v-slot:prepend>
          <q-icon name="event" />
        </template>
      </q-input>

      <q-input rounded outlined v-model="text">
        <template v-slot:append>
          <q-avatar>
            <img src="https://cdn.quasar-framework.org/img/quasar-logo.png">
          </q-avatar>
        </template>
      </q-input>

      <q-input rounded standout bottom-slots v-model="text" label="Label" counter>
        <template v-slot:prepend>
          <q-icon name="place" />
        </template>
        <template v-slot:append>
          <q-icon name="close" @click="text = ''" class="cursor-pointer" />
        </template>

        <template v-slot:hint>
          Field hint
        </template>
      </q-input>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      text: ''
    }
  }
}
</script>

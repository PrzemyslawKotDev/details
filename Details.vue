<template>
  <div class="q-pa-mg">
    <q-btn label="Open Dialog" color="primary" @click="dialog = true" />

    <q-dialog v-model="dialog">
      <q-card style="width: 40%">
        <q-card-section>
          <div class="text-h6 border-bottom">Item info</div>

          <!-- v-for i pętla przez dane w siatkę -->

            <div class="row">
                <div class="col-12 col-md-3">User:</div>
                <div class="col-12 col-md-9">Przemysław Kot</div>
            </div>
            <div class="row">
                <div class="col-12 col-md-3">Supervisor:</div>
                <div class="col-12 col-md-9">Filip</div>
            </div>
            
        </q-card-section>

        <q-card-actions align="around">

          <q-btn label="Return" color="red" @click="dialog2 = true" />
          <q-btn label="Extend" color="primary" @click="dialog2 = true" />

        </q-card-actions>

      </q-card>
    </q-dialog>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      dialog: ref(false),
      dialog2: ref(false)
    }
  }
}
</script>

<style lang="sass" scoped>
.row > div
  padding: 10px 15px
  background: rgba(86,61,124,.15)
  border-bottom: 1px solid rgba(86,61,124,.2)
  border-left: 1px solid rgba(86,61,124,.2)
  border-right: 1px solid rgba(86,61,124,.2)
.border-bottom
  border-bottom: 1px solid rgba(86,61,124,.2)
</style>
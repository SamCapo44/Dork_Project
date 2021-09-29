<template>
  <q-page class="relative-position">
      <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
        <div class="col">
          <q-input
            v-model="newDorkContent"
            class="new-dork"
            placeholder="What's happening?"
            maxlength="280"
            bottom-slots
            counter
            autogrow
          >
            <template v-slot:before>
              <q-avatar size="xl">
                <img src="https://cdn.quasar.dev/img/avatar5.jpg">
              </q-avatar>
            </template>
          </q-input>
        </div>
        <div class="col col-shrink">
          <q-btn
            @click="addNewDork"
            :disable="!newDorkContent"
            class="q-mb-lg"
            color="primary"
            label="Dork"
            rounded
            unelevated
            no-caps
          />
        </div>
      </div>

     <q-separator  
      class="divider"
      size="10px"
      color="grey-2"
     />
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PageHome',
  data() {
    return {
      newDorkContent: ''
    }
  }
})
</script>

<style lang="sass">
.new-dork
  textarea
    font-size: 19px
    line-height: 1.44 !important
  .divider
    boreder-top: 1px solid
    boreder-bottom: 1px solid
    boreder-color: $grey-4
</style>
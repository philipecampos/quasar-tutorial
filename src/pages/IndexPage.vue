<template>
  <q-page class="row">
    <q-card class="col-xs-9">
      <q-toolbar>
        <q-input
          :model-value="search"
          borderless
          class="full-width"
          dense
          placeholder="Search"
        >
          <template #append>
            <q-icon name="mdi-magnify"></q-icon>
          </template>
        </q-input>
      </q-toolbar>

      <q-list bordered>
        <q-item>
          <q-item-section side>
            <q-checkbox :model-value="true" />
          </q-item-section>

          <q-item-section> Go Shopping</q-item-section>

          <q-item-section side>
            <q-btn flat icon="mdi-delete" round size="sm"></q-btn>
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>

    <div class="col-xs-3">
      <q-toolbar class="bg-primary">
        <q-btn
          class="q-ml-lg"
          color="secondary"
          fab
          icon="mdi-plus"
          style="margin-bottom: -42px"
        ></q-btn>
      </q-toolbar>
    </div>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
      search: '',
    };
  },
});
</script>

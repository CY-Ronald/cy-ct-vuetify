<template>
  <v-dialog v-model="show">
    <v-card>
      <v-card-row v-if="title">
        <v-card-title>{{ title }}</v-card-title>
      </v-card-row>
      <v-card-row v-if="body">
        <v-card-text>{{ body }}</v-card-text>
      </v-card-row>
      <v-card-row actions>
        <v-btn
          class="green--text darken-1"
          flat="flat"
          @click.native="onCancel"
          v-if="cancel"
          >{{ cancel }}</v-btn
        >
        <v-btn
          class="green--text darken-1"
          flat="flat"
          @click.native="onOk"
          v-if="ok"
          >{{ ok }}</v-btn
        >
      </v-card-row>
    </v-card>
  </v-dialog>
</template>
<script>
export default {
  props: ["title", "body", "ok", "cancel", "show"],
};
</script>
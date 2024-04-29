<template>
  <v-row class="d-flex justify-center align-center fill-height" style="min-height: 100vh">
    <v-col cols="12" md="6">
      <v-card class="py-6">
        <v-card-title class="d-flex justify-center">
          <div class="text-h4">
            Add Place
          </div>
        </v-card-title>
        <v-card-text>
          <v-text-field
              label="Add Place name"
              outlined
          ></v-text-field>
          <v-text-field
              label="Add Openhours"
              outlined
          ></v-text-field>
          <v-text-field
              label="Add Location"
              outlined
          ></v-text-field>
          <v-text-field
              label="Add a description"
              outlined
          ></v-text-field>
          <v-file-input
 label="Upload Image"
 outlined
 accept="image/*"
 @change="onFileSelected"
></v-file-input>
          <div class="text-right">
            <v-btn color="primary">
              Add place
            </v-btn>
          </div>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

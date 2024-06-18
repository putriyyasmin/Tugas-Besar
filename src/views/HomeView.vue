<script setup lang="ts">
import TheWelcome from '../components/TheWelcome.vue'
</script>

<template>
    <div class="container mt-10"></div>
    <div style="margin-left: -10px">
      <div style="width: 100%;" class="mt-5">
        <div style="margin-left: -100px">
          <v-row>
            <v-col cols="12" md="2">
              <v-card
                text="8"
                title="Total Peserta"
              ></v-card>
            </v-col>
          </v-row>

          <v-row>
            <v-col cols="12" md="2">
              <v-card
                text="8"
                title="Jumlah Pendaftar"
              ></v-card>
            </v-col>
          </v-row>

          <v-row>
            <v-col cols="12" md="2">
              <v-card
                text="8"
                title="Universitas"
              ></v-card>
            </v-col>
          </v-row>
        </div>
      </div>
    </div>
</template>

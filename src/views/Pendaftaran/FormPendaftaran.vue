<template>
    <div style="margin-left: -350px">
        <div class="container mt-10">
            <div class="card">
                <div style="width: 100%" class="mt-1">
                        <div style="margin-left: 5px">
                            <div class="card-header">
                                <h4>Form Pendaftaran</h4>
                            </div>
                                <v-sheet class="mx-auto" width="1000">
                                    <v-container>
                                        <v-row>
                                            <v-col cols="12">
                                                <v-text-field label="Nama Peserta" variant="outlined" v-model="psn.nama"></v-text-field>
                                            </v-col>
                                        </v-row>
                                        <v-row>
                                            <v-col cols="12">
                                                <v-text-field label="Universitas" v-model="psn.universitas" variant="outlined"></v-text-field>
                                            </v-col>
                                        </v-row>
                                        <v-row>
                                            <v-col cols="12">
                                                <v-combobox
                                                    label="Kategori Lomba"
                                                    v-model="psn.lomba"
                                                    :items="['Basket', 'Volly', 'Futsal', 'Panahan', 'Renang']"
                                                    variant="outlined"
                                                ></v-combobox>
                                            </v-col>
                                        
                                        </v-row>
                                        <v-row>
                                            <v-col cols="12">
                                                <v-combobox
                                                    label="Kategori Peserta"
                                                    v-model="psn.kategori"
                                                    :items="['Putra', 'Putri']"
                                                    variant="outlined"
                                                ></v-combobox>
                                            </v-col>
                                        </v-row>
                                        <v-row>
                                            <v-col cols="12">
                                                <v-btn color="blue" @click="submitLomba">SUBMIT</v-btn>
                                            </v-col>
                                        </v-row>
                                    </v-container>
                                </v-sheet>
                        </div>
                </div>
            </div>
        </div>
    </div>
</template>
  <script lang="ts">
  import {Lomba} from '@/model/Lomba'
  export default{
      data(){
          return{
              psn: new Lomba ('', ' ',' ',' ')
          }
      },
      methods:{
          submitLomba(){
              alert('Data Lomba ' + this.psn.nama + ' berhasil ditambahkan')
          }
      }
  }
  </script>
  
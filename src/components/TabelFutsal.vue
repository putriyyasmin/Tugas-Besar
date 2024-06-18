<template>
    <v-table>
      <thead>
        <tr>
          <th class="text-left">
            Nama
          </th>
          <th class="text-left">
            Universitas
          </th>
          <th class="text-left">
            Kategori Lomba
          </th>
          <th class="text-left">
            Kategori
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in Lomba"
          :key="item.nama"
        >
          <td>{{ item.nama }}</td>
          <td>{{ item.universitas }}</td>
          <td>{{ item.lomba }}</td>
          <td>{{ item.kategori }}</td>
        </tr>
      </tbody>
    </v-table>
  </template>
  <script>
    export default {
      data () {
        return {
          Lomba: [
            {
              nama: 'Tim BSK',
              universitas: 'adalah',
              lomba:'Basket',
              kategori:'Putra',
            },
            {
              nama: 'Tim BSK',
              universitas: 'adalah',
              lomba:'Futsal',
              kategori:'Putra',
            },
          ],
        }
      },
    }
  </script>
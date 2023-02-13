<template>
  <div class="ml-auto w-52">
    TailwindCSS
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <v-combobox v-model="select" :items="items" label="Группы" multiple outlined dense></v-combobox>
        </v-col>
      </v-row>
    </v-container>
    <v-btn @click="getSelected" color="accent" elevation="14">Получить выбранные группы</v-btn>
  </div>

  <v-container fluid>
    <v-row>
      <v-col cols="12">
        <v-combobox v-model="select" :items="items" label="Группы" multiple outlined dense></v-combobox>
      </v-col>
    </v-row>
  </v-container>
  <v-btn @click="getSelected" color="accent" elevation="14">Получить выбранные группы</v-btn>
</template>

<script>
export default {
  // Option API
  data() {
    return {
      select: [],
      items: [
        'фыва',
        'Design',
        'Vue',
        'Vuetify',
      ],
    }
  },
  methods: {
    getSelected() {
      console.log(this.select) 
    }
  },
  // Composition API
  setup() {
    const getSelectedComposAPI = () => {
      console.log('Hi')
    }

    return { getSelectedComposAPI };
  },
}


</script>

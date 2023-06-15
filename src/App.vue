<template>
   <v-app id="inspire">
    <v-system-bar>
      
    </v-system-bar>

    <v-navigation-drawer v-model="drawer">
      <v-sheet
        color="grey-lighten-4"
        class="pa-4"
      >
        <v-avatar
          class="mb-4"
          color="grey-darken-1"
          size="64"
        ></v-avatar>

        <div>raicivan06@gmail.com</div>
      </v-sheet>

      <v-divider></v-divider>

      <v-list>
        <v-list-item
          
          v-for="[icon, text] in links"
          :key="icon"
          link
        >
          <template v-slot:prepend>
            <v-icon>{{ icon }}</v-icon>
          </template>

          <v-list-item-title>{{ text }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>

   
</template>

<script setup>
  import { ref } from 'vue'

 
  const links = [
    ['mdi-inbox-arrow-down', 'Dodaj'],
    
  ]

  const drawer = ref(null)
</script>

<script>
  export default {
    data: () => ({
      cards: ['Today', 'Yesterday'],
      drawer: null,
      links: [
        ['mdi-inbox-arrow-down', 'Inbox'],
        
      ],
    }),
  }
</script>
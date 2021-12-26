<template>
  <v-app >
     <v-app-bar
      color="blue darken-1"
      app
    >
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>TODO LIST</v-toolbar-title>
    </v-app-bar>

<v-navigation-drawer
      v-model="drawer"
      src="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
     app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
     </v-navigation-drawer>

   
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer : false,
    group : null,
    items : [
      {
          icon: 'mdi-email',
          text: 'Inbox',
        },
        {
          icon: 'mdi-account-supervisor-circle',
          text: 'Star',
        },
        {
          icon: 'mdi-clock-start',
          text: 'Send',
        },
        {
          icon: 'mdi-email-open',
          text: 'Drafts',
        },
    ]

  }),
};
</script>

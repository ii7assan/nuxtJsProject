<template>
  <div>
    <v-toolbar height="70px" color="white" dark fixed>
      <v-toolbar-title class="display-1 black--text"
        >همزبان - Hamzabaan</v-toolbar-title
      >
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <!-- <v-btn class="transparent mx-1" v-for="item in menu" :key="item.icon" plain>{{
            item.name
          }}</v-btn> -->
        <v-btn plain class="black--text">خانه</v-btn>
        <v-btn class="amber darken-1 rounded-xl">ورود/ ثبت نام</v-btn>
      </v-toolbar-items>
      <v-app-bar-nav-icon
        class="hidden-md-and-up black--text"
        @click.stop="drawer = !drawer"
      ></v-app-bar-nav-icon>
    </v-toolbar>
    <v-navigation-drawer v-model="drawer" :right="right" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>Foo</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      group: null,
      right: true,
      menu: [
        {
          name: "home",
        },
        {
          name: "profile",
        },
        {
          name: "exit",
        },
      ],
    };
  },
};
</script>

<style>
</style>
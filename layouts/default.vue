<template>
  <v-app dark>
    <v-navigation-drawer class="hidden-md-and-up"
      v-model="drawer"
     
      
      fixed
    >

    <div class="pa-6">
      <img src="../static/assets/Logo.svg" alt="">
    </div>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon small>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar style="border-bottom: 1px solid #ddd !important;" height="70px" class="white  nav-bar" fixed app flat>
      <img src="../static/assets/Logo.svg" class="mr-3" alt="" />

   
      <v-btn class="nav-item hidden-sm-and-down" text>Home</v-btn>
      <v-btn class="nav-item hidden-sm-and-down" text>Dashboard</v-btn>
      <v-btn class="nav-item hidden-sm-and-down" text>Projects</v-btn>
      <v-btn class="nav-item hidden-sm-and-down" text>Tasks</v-btn>
      <v-btn class="nav-item hidden-sm-and-down" text>Reporting</v-btn>
      <v-btn class="nav-item hidden-sm-and-down" text>Users</v-btn>

      <v-spacer></v-spacer>

      <v-btn class="upgrade-btn hidden-sm-and-down" height="40px">
        <img src="../static/assets/flash.svg" alt="" class="mr-2"/> Upgrade Now</v-btn
      >

      <v-btn icon class="mx-2 hidden-sm-and-down"><img src="../static/assets/settings.svg" alt=""></v-btn>
      <v-btn icon class="mx-2 hidden-sm-and-down"><img src="../static/assets/notification.svg" alt=""></v-btn>
      <v-avatar class="hidden-sm-and-down">
        <img src="../static/assets/Avatar.svg" alt="">
      </v-avatar>


      <v-btn icon class="hidden-md-and-up"
        @click.stop="drawer = !drawer"><img src="../static/assets/hamburger.svg" alt="">

      </v-btn>
    </v-app-bar>
    <v-app-bar  height="70px" class="white nav-bar hidden-sm-and-down " style="margin-top: 70px; border-bottom: 1px solid #ddd !important;" fixed flat>
      <v-btn class="nav-item pl-0 ml-0" text>Overview</v-btn>
      <v-btn class="nav-item" text>Notifications</v-btn>
      <v-btn class="nav-item" text>Analytics</v-btn>
      <v-btn class="nav-item" text>Saved reports</v-btn>
      <v-btn class="nav-item" text>Trade history</v-btn>
      <v-btn class="nav-item" text>User reports</v-btn>
      <v-spacer></v-spacer>

      <v-text-field outlined prepend-inner-icon="search" placeholder="Search" dense class="mt-6"></v-text-field>
    </v-app-bar>
    <v-main>
      <v-container fluid :class="{'container' : $vuetify.breakpoint.mdAndUp}">
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light> mdi-repeat </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'fi fi-rr-home',
          title: 'Home',
          to: '/',
        },
        {
          icon: 'fi fi-rr-apps',
          title: 'Dashboard',
          to: '/#dashboard',
        },
        {
          icon: 'fi fi-rr-edit-alt',
          title: 'Projects',
          to: '/#projects',
        },
        {
          icon: 'fi fi-rr-list-check',
          title: 'Tasks',
          to: '/#tasks',
        },
        {
          icon: 'fi fi-rr-mobile',
          title: 'Reporting',
          to: '/#reporting',
        },
        {
          icon: 'fi fi-rr-user',
          title: 'Users',
          to: '/#users',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.nav-bar {
  border-bottom: 1px solid #ddd !important;
  padding-right: 5%;
  padding-left: 5%;
  .nav-item {
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    /* identical to box height, or 150% */

    /* Gray/700 */

    color: #344054;

    /* Inside auto layout */

    flex: none;
    order: 0;
    flex-grow: 0;
    margin: 0px 12px;
  }

  .v-btn {
    text-transform: inherit !important;
  }

  .upgrade-btn {
    background: #ffffff;
    /* Gray/300 */

    border: 1px solid #d0d5dd;
    box-sizing: border-box;
    /* Shadow/xs */

    box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
    border-radius: 8px;

    flex: none;
    order: 0;
    flex-grow: 0;
    margin: 0px 0px;
  }
}
.container{
  padding-right: 6%;
  padding-left: 6%;
}
</style>
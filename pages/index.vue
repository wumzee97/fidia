<template>
  <div
    class="pb-16"
    :class="{
      'pt-16': $vuetify.breakpoint.mdAndUp,
      'pt-8': $vuetify.breakpoint.smAndDown,
    }"
  >
    <v-row
      :class="{
        'pt-10': $vuetify.breakpoint.mdAndUp,
      }"
    >
      <v-col md="6" cols="12">
        <h3 class="welcome">Welcome back, Olivia</h3>
        <p class="sub-text">
          Track, manage and forecast your customers and orders.
        </p>
      </v-col>
      <v-col
        md="6"
        cols="12"
        :class="{ 'text-right': $vuetify.breakpoint.mdAndUp }"
      >
        <v-btn class="import-btn" text height="40px">
          <img src="../static/assets/import.svg" class="mr-2" alt="" />
          Import</v-btn
        >
        <v-btn class="add-btn ml-3" text height="40px"
          ><v-icon class="mr-1">add</v-icon> Add</v-btn
        >
      </v-col>
    </v-row>

    <v-row class="mt-4">
      <v-col md="4">
        <v-card flat class="summary-card pa-6">
          <div class="d-flex justify-space-between">
            <p class="titles">Total customers</p>
            <v-menu
              bottom
              left
              offset-y
              class="elevation-0"
              origin="top right"
              transition="scale-transition"
            >
              <template v-slot:activator="{ attrs, on }">
                <v-btn icon v-bind="attrs" v-on="on">
                  <v-icon size="20">more_vert</v-icon></v-btn
                >
              </template>

              <v-list dense flat class="py-">
                <v-list-item class="py-0 my-0">
                  <v-list-item-content class="py-0 my-0">
                    <v-list-item-title>View Details </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-list-item @click="null" class="py-0 my-0">
                  <v-list-item-content>
                    <v-list-item-title>Review Item </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-menu>
          </div>

          <div class="d-flex justify-space-between mt-4">
            <div>
              <p class="text mb-">2,420</p>
              <p class="label mb-0">
                <v-icon color="#12B76A">arrow_upward</v-icon>
                <span class="up">40%</span> vs last month
              </p>
            </div>
            <img src="../static/assets/chart1.svg" alt="" />
          </div>
        </v-card>
      </v-col>

      <v-col md="4">
        <v-card flat class="summary-card pa-6">
          <div class="d-flex justify-space-between">
            <p class="titles">Members</p>
            <v-menu
              bottom
              left
              offset-y
              class="elevation-0"
              origin="top right"
              transition="scale-transition"
            >
              <template v-slot:activator="{ attrs, on }">
                <v-btn icon v-bind="attrs" v-on="on">
                  <v-icon size="20">more_vert</v-icon></v-btn
                >
              </template>

              <v-list dense flat class="py-">
                <v-list-item class="py-0 my-0">
                  <v-list-item-content class="py-0 my-0">
                    <v-list-item-title>View Details </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-list-item @click="null" class="py-0 my-0">
                  <v-list-item-content>
                    <v-list-item-title>Review Item </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-menu>
          </div>

          <div class="d-flex justify-space-between mt-4">
            <div>
              <p class="text mb-">1,210</p>
              <p class="label mb-0">
                <v-icon color="#F04438">arrow_downward</v-icon>
                <span class="down">10%</span> vs last month
              </p>
            </div>
            <img src="../static/assets/chart2.svg" alt="" />
          </div>
        </v-card>
      </v-col>

      <v-col md="4">
        <v-card flat class="summary-card pa-6">
          <div class="d-flex justify-space-between">
            <p class="titles">Active now</p>
            <v-menu
              bottom
              left
              offset-y
              class="elevation-0"
              origin="top right"
              transition="scale-transition"
            >
              <template v-slot:activator="{ attrs, on }">
                <v-btn icon v-bind="attrs" v-on="on">
                  <v-icon size="20">more_vert</v-icon></v-btn
                >
              </template>

              <v-list dense flat class="py-">
                <v-list-item class="py-0 my-0">
                  <v-list-item-content class="py-0 my-0">
                    <v-list-item-title>View Details </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>

                <v-list-item @click="null" class="py-0 my-0">
                  <v-list-item-content>
                    <v-list-item-title>Review Item </v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </v-menu>
          </div>

          <div class="d-flex justify-space-between mt-4">
            <div>
              <p class="text mb-">316</p>
              <p class="label mb-0">
                <v-icon color="#12B76A">arrow_upward</v-icon>
                <span class="up">20%</span> vs last month
              </p>
            </div>
            <img src="../static/assets/chart1.svg" alt="" />
          </div>
        </v-card>
      </v-col>
    </v-row>

    <v-row class="mt-8">
      <v-col md="9" class="hidden-sm-and-down" cols="12">
        <v-chip class="chips" close close-icon="close">All time</v-chip>
        <v-chip class="chips ml-2" close close-icon="close">US, AU, +4</v-chip>
        <v-btn class="chips-more ml-2"
          ><v-icon class="mr-1">filter_list</v-icon> More filters</v-btn
        >
      </v-col>
      <v-col md="3" align-self="right" cols="12">
        <v-text-field
          outlined
          dense
          prepend-inner-icon="search"
          placeholder="Search"
        >
        </v-text-field>
        <div class="hidden-md-and-up">
          <v-btn style="width: 100%" class="chips-more"
            ><v-icon class="mr-1">filter_list</v-icon> More filters</v-btn
          >
          <v-chip class="chips my-6" close close-icon="close">All time</v-chip>
          <v-chip class="chips ml-2 my-6" close close-icon="close"
            >US, AU, +4</v-chip
          >
        </div>
      </v-col>
    </v-row>

    <v-card class="table-card">
      <v-data-table
        mobile-breakpoint="0"
        v-model="selectedCompanies"
        item-key="id"
        :headers="headers"
        :items="items"
        hide-default-footer
        show-select
      >
        <template v-slot:item.company="{ item }">
          <div class="d-flex align-center">
            <v-avatar size="40px">
              <img :src="item.logo" alt="" />
            </v-avatar>
            <div class="ml-3">
              <p class="name my-0">{{ item.company }}</p>
              <p class="label my-0">{{ item.url }}</p>
            </div>
          </div>
        </template>
        <template v-slot:item.license_use="{ item }">
          <v-progress-linear
            :value="item.license_use"
            height="8px"
            class="rounded"
          ></v-progress-linear>
        </template>
        <template v-slot:item.status="{ item }">
          <v-chip
            :class="
              item.status == 'Customer' ? 'chip-customer' : 'chip-churned'
            "
            >{{ item.status }}</v-chip
          >
        </template>
        <template v-slot:item.users="{ item }">
          <div class="d-flex">
            <v-avatar class="avatar" size="34px" v-for="i in 5" :key="i">
              <img :src="require(`../static/assets/Avatar${i}.svg`)" alt="" />
            </v-avatar>
            <div class="more-avatar d-flex align-center justify-center">+5</div>
          </div>
        </template>
        <template v-slot:item.about="{ item }">
          <p class="name my-0">{{ item.about.title }}</p>
          <p class="label my-0">{{ item.about.description }}</p>
        </template>

        <template v-slot:item.actions="{  }">
          <v-btn icon>
            <v-icon size="17">fi fi-rr-trash</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon size="17">fi fi-rr-pencil</v-icon>
          </v-btn>
        </template>
      </v-data-table>
      <div class="hidden-sm-and-down">
      <div class="d-flex justify-space-between align-center pa-4">
        <div>
          <v-btn text class="pagination-btn">Previous</v-btn>
          <v-btn text class="pagination-btn ml-2">Next</v-btn>
        </div>
        <p class="my-0 pagination-text">Page 1 of 10</p>
      </div>

      </div>
       <div class="hidden-md-and-up">
      <div class="d-flex justify-space-between align-center pa-4">
        
          <v-btn icon><v-icon>west</v-icon></v-btn>
        <p class="my-0 pagination-text">Page 1 of 10</p>
          <v-btn icon><v-icon>east</v-icon></v-btn>
        
      </div>

      </div>

    </v-card>
  </div>
</template>
<script>
export default {
  data: () => ({
    selectedCompanies: [],
    headers: [
      { text: 'Company', value: 'company' },
      { text: 'License use', value: 'license_use' },
      { text: 'Status', value: 'status' },

      { text: 'Users', value: 'users' },
      { text: 'About', value: 'about' },
      { text: '', value: 'actions' },
    ],
    items: [
      {
        id: 1,
        company: 'Catalog',
        url: 'catalogapp.io',
        logo: require('../static/assets/catalog.svg'),
        license_use: 80,
        status: 'Customer',
        about: {
          title: 'Content curating app',
          description: 'Brings all your news into one place',
        },
      },
      {
        id: 2,
        company: 'Circooles',
        url: 'getcirooles.com',
        logo: require('../static/assets/circooles.svg'),
        license_use: 70,
        status: 'Churned',
        about: {
          title: 'Design software',
          description: 'Super lightweight design app',
        },
      },
      {
        id: 3,
        company: 'Command+R',
        url: 'cmdr.ai',
        logo: require('../static/assets/commandr.svg'),
        license_use: 40,
        status: 'Customer',
        about: {
          title: 'Data prediction',
          description: 'AI and machine learning data',
        },
      },
      {
        id: 4,
        company: 'Hourglass',
        url: 'hourglass.app',
        logo: require('../static/assets/hourglass.svg'),
        license_use: 90,
        status: 'Customer',
        about: {
          title: 'Productivity app',
          description: 'Time management and productivity',
        },
      },
      {
        id: 5,
        company: 'Layers',
        url: 'getlayers.io',
        logo: require('../static/assets/layers.svg'),
        license_use: 30,
        status: 'Churned',
        about: {
          title: 'Web app integrations',
          description: 'Connect web apps seamlessly',
        },
      },
      {
        id: 6,
        company: 'Quotient',
        url: 'quotient.co',
        logo: require('../static/assets/quotient.svg'),
        license_use: 20,
        status: 'Customer',
        about: {
          title: 'Sales CRM',
          description: 'Web-based sales doc management',
        },
      },
      {
        id: 7,
        company: 'Sisyphus',
        url: 'sisyphus.com',
        logo: require('../static/assets/sisyphus.svg'),
        license_use: 50,
        status: 'Customer',
        about: {
          title: 'Automation and workflow',
          description: 'Time tracking, invoicing and expenses',
        },
      },
    ],
  }),
}
</script>

<style lang="scss" scoped>
.welcome {
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 30px;
  line-height: 38px;
  /* identical to box height, or 127% */

  /* Gray/900 */

  color: #101828;
}
.sub-text {
  font-family: Inter;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 24px;
  /* identical to box height, or 150% */

  /* Gray/500 */

  color: #667085;
}
.import-btn {
  background: #ffffff;
  /* Gray/300 */

  border: 1px solid #d0d5dd;
  box-sizing: border-box;
  /* Shadow/xs */

  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 8px;
  /* Text sm/Medium */

  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  /* Gray/700 */

  color: #344054;
}
.add-btn {
  background: #7f56d9 !important;
  /* Primary/600 */

  border: 1px solid #7f56d9;
  box-sizing: border-box;
  /* Shadow/xs */

  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 8px;
  /* Text sm/Medium */

  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  /* White */

  color: #ffffff;
}
.v-btn {
  text-transform: inherit !important;
}
.summary-card {
  background: #ffffff;
  /* Gray/200 */

  border: 1px solid #eaecf0;
  box-sizing: border-box;
  /* Shadow/sm */

  box-shadow: 0px 1px 3px rgba(16, 24, 40, 0.1),
    0px 1px 2px rgba(16, 24, 40, 0.06);
  border-radius: 8px;
  .titles {
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    /* identical to box height, or 150% */

    /* Gray/900 */

    color: #101828;
  }
  .text {
    font-family: Inter;
    font-style: normal;
    font-weight: 600;
    font-size: 36px;
    line-height: 44px;
    /* identical to box height, or 122% */

    letter-spacing: -0.02em;

    /* Gray/900 */

    color: #101828;
  }
  .label {
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    /* identical to box height, or 143% */

    /* Gray/500 */

    color: #667085;
  }
  span.up {
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    /* identical to box height, or 143% */

    text-align: center;

    /* Success/700 */

    color: #027a48;
  }
  .span.down {
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    /* identical to box height, or 143% */

    text-align: center;

    /* Error/700 */

    color: #b42318;
  }
}
.chips {
  background: #f9f5ff !important;
  /* Primary/50 */
  height: 40px;

  border: 1px solid #f9f5ff;
  box-sizing: border-box;
  /* Shadow/xs */

  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05) !important;
  border-radius: 8px;

  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  /* Primary/700 */

  color: #6941c6;
}
.chips-more {
  background: #ffffff !important;
  /* Gray/300 */
  height: 40px;

  border: 1px solid #d0d5dd;
  box-sizing: border-box;
  /* Shadow/xs */

  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 8px;
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  /* Gray/700 */

  color: #344054;
}
.table-card {
  background: #ffffff;
  /* Gray/200 */

  border: 1px solid #eaecf0;
  box-sizing: border-box;
  /* Shadow/md */

  box-shadow: 0px 4px 8px -2px rgba(16, 24, 40, 0.1),
    0px 2px 4px -2px rgba(16, 24, 40, 0.06) !important;
  border-radius: 8px;

  .name {
    /* Text sm/Medium */

    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    /* identical to box height, or 143% */

    /* Gray/900 */

    color: #101828;
  }
  .label {
    font-family: Inter;
    font-style: normal;
    font-weight: normal;
    font-size: 14px;
    line-height: 20px;
    /* identical to box height, or 143% */

    /* Gray/500 */

    color: #667085;
  }
}
.chip-customer {
  /* Success/50 */
  height: 22px;
  background: #ecfdf3 !important;
  border-radius: 16px;
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 18px;
  /* identical to box height, or 150% */

  text-align: center;

  /* Success/700 */

  color: #027a48;
}
.chip-churned {
  /* Gray/100 */
  height: 22px;
  background: #f2f4f7 !important;
  border-radius: 16px;
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 18px;
  /* identical to box height, or 150% */

  text-align: center;

  /* Gray/700 */

  color: #344054;
}

.avatar {
  margin-left: -10px;
}
.more-avatar {
  background: #f9f5ff;
  margin-left: -10px;
  z-index: 1;
  /* White */

  border: 2px solid #ffffff;
  border-radius: 200px;
  height: 34px;
  width: 34px;
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 18px;
  /* identical to box height, or 150% */

  text-align: center;

  /* Primary/600 */

  color: #7f56d9;
}

.pagination-btn {
  background: #ffffff;
  /* Gray/300 */

  border: 1px solid #d0d5dd !important;
  box-sizing: border-box;
  height: 38px !important;
  /* Shadow/xs */

  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05) !important;
  border-radius: 6px;
  font-family: Inter;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  /* Gray/700 */

  color: #344054;
}
.pagination-text {
  font-family: Inter;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 20px;
  /* identical to box height, or 143% */

  /* Gray/700 */

  color: #344054;
}

@media only screen and (max-width: 600px) {
  .welcome {
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 24px;
    line-height: 32px;
    /* identical to box height, or 133% */

    /* Gray/900 */

    color: #101828;
  }

  .summary-card {
    .text {
      font-family: Inter;
      font-style: normal;
      font-weight: 600;
      font-size: 30px;
      line-height: 38px;
      /* identical to box height, or 127% */

      /* Gray/900 */

      color: #101828;
    }
    img{
      width: 96px;
    }
  }
}
</style>
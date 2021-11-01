<template>
  <div>
    <v-responsive>
      <v-app :style="{ background: $vuetify.theme.themes.light.background }">
        <v-container>
          <v-layout row class="ma-4">
            <v-app style="background-color: rgb(170, 31, 170)" class="rounded">
              <v-row>
                <v-col cols="12" md="8" class="ligne">
                  <v-container>
                    <v-row>
                      <v-col cols="12" md="7" sm="7">
                        <v-text-field
                          label="search"
                          prepend-icon="mdi-search"
                        ></v-text-field>
                      </v-col>

                      <v-col cols="12" md="12">
                        <h1 class="headline mb-2 green--text">money status</h1>

                        <template
                          ><div id="app">
                            <GChart
                              type="ColumnChart"
                              :data="chartData"
                              :options="chartOptions"
                            />
                          </div>
                        </template>
                      </v-col>
                      <v-col cols="12" md12
                        ><h1 class="headline mb-2 green--text">budgets</h1>
                      </v-col>
                      <v-col cols="12" md="8">
                        <v-card>
                          <v-list>
                            <v-list-item>
                              <v-list-item-avatar color="blue">
                                <v-icon dark>fas fa-car</v-icon>
                              </v-list-item-avatar>
                              <v-list-item-content>
                                <v-list-item-title>auto & transparent</v-list-item-title>
                                <v-list-item-subtitle>700$ left</v-list-item-subtitle>
                              </v-list-item-content>
                              <v-list-item-content align="right">
                                <v-list-item-title class="purple--text"
                                  >$1,200</v-list-item-title
                                >
                                <v-list-item-subtitle>$500 of 1.200</v-list-item-subtitle>
                              </v-list-item-content>
                            </v-list-item>
                            <v-divider inset class="purple"></v-divider>
                            <v-list-item>
                              <v-list-item-avatar color="red">
                                <v-icon dark>fas fa-utensils</v-icon>
                              </v-list-item-avatar>
                              <v-list-item-content>
                                <v-list-item-title>food & drinks</v-list-item-title>
                                <v-list-item-subtitle>7$ left</v-list-item-subtitle>
                              </v-list-item-content>
                              <v-list-item-content align="right">
                                <v-list-item-title class="purple--text"
                                  >$1000</v-list-item-title
                                >

                                <v-list-item-subtitle>$500 of 400</v-list-item-subtitle>
                              </v-list-item-content>
                            </v-list-item>
                            <v-divider inset class="purple"></v-divider>
                            <v-list-item>
                              <v-list-item-avatar color="yellow">
                                <v-icon dark> fas fa-user-graduate</v-icon>
                              </v-list-item-avatar>
                              <v-list-item-content>
                                <v-list-item-title>student</v-list-item-title>
                                <v-list-item-subtitle>400$ left</v-list-item-subtitle>
                              </v-list-item-content>
                              <v-list-item-content align="right">
                                <v-list-item-title class="purple--text"
                                  >$500</v-list-item-title
                                >
                                <v-list-item-subtitle>$500 of 4040</v-list-item-subtitle>
                              </v-list-item-content>
                            </v-list-item>
                            <v-divider inset class="purple"></v-divider>
                            <v-list-item>
                              <v-list-item-avatar color="green" height>
                                <v-icon dark>fas fa-dumbbell</v-icon>
                              </v-list-item-avatar>
                              <v-list-item-content>
                                <v-list-item-title>sport</v-list-item-title>
                                <v-list-item-subtitle>9000$ left</v-list-item-subtitle>
                              </v-list-item-content>
                              <v-list-item-content align="right">
                                <v-list-item-title class="purple--text"
                                  >$1,800</v-list-item-title
                                >
                                <v-list-item-subtitle>$200 of 400</v-list-item-subtitle>
                              </v-list-item-content>
                            </v-list-item>
                            <v-divider inset class="purple"></v-divider>
                          </v-list>
                        </v-card>
                      </v-col>
                      <v-col cols="12" md="4">
                        <v-card class="max-auto" max-height="350">
                          <v-img
                            class="purple--text align-end"
                            height="150px"
                            src="../views/card.jpg"
                          ></v-img>
                          <v-card-title class="pb-0">cash loan</v-card-title>
                          <v-card-text class="text--primary">
                            <div>up to 2 million dollar</div>
                            <div>money the next data.rate</div>
                          </v-card-text>
                        </v-card>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-col>
                <v-col cols="12" md="4">
                  <v-container>
                    <v-row>
                      <v-col cols="12" md="12">
                        <v-list-item>
                          <v-list-item-avatar>
                            <v-img src="/views/card.jpg"></v-img>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-title>fahad samara</v-list-item-title>
                            <v-list-item-subtitle class="red--white"
                              >fahad0smara@gmail.com</v-list-item-subtitle
                            >
                          </v-list-item-content>

                          <v-list-item-action>
                            <v-icon>fas fa-sign-out-alt</v-icon>
                          </v-list-item-action>
                        </v-list-item>
                        <v-divider class="white"></v-divider>
                      </v-col>

                      <v-col cols="12" md12>
                        <v-list-item>
                          <v-list-item-avatar color="grey">
                            <v-icon color="white">fas fa-dollar-sign</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-subtitle>Heisenberg</v-list-item-subtitle>
                            <v-list-item-title>$15.423</v-list-item-title>
                          </v-list-item-content>
                          <v-list-item-action>
                            <v-icon color="white" large>fab fa-cc-visa</v-icon>
                          </v-list-item-action>
                        </v-list-item>
                        <v-list-item>
                          <v-list-item-avatar color="grey">
                            <v-icon color="white">fas fa-dollar-sign</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-subtitle>Heisenberg</v-list-item-subtitle>
                            <v-list-item-title>$15.423</v-list-item-title>
                          </v-list-item-content>
                          <v-list-item-action>
                            <v-icon color="black" large>fab fa-cc-mastercard</v-icon>
                          </v-list-item-action>
                        </v-list-item>
                        <v-list-item>
                          <v-list-item-avatar color="grey">
                            <v-icon color="white">fas fa-dollar-sign</v-icon>
                          </v-list-item-avatar>
                          <v-list-item-content>
                            <v-list-item-subtitle>Heisenberg</v-list-item-subtitle>
                            <v-list-item-title>$15.423</v-list-item-title>
                          </v-list-item-content>
                          <v-list-item-action>
                            <v-icon color="green" large>fab fa-cc-paypal</v-icon>
                          </v-list-item-action>
                        </v-list-item>
                        <v-col cols="12" md12>
                          <v-list-item>
                            <v-list-item-avatar color="indigo">
                              <v-icon color="white">fas fa-plus</v-icon>
                            </v-list-item-avatar>
                            <v-list-item-title>Add card card</v-list-item-title>
                          </v-list-item>
                          <v-col cols="12" md12>
                            <v-card color="white--text " dark>
                              <div class="d-flex flex-no-wrap justify-space-between">
                                <div>
                                  <v-card-title class="headline"
                                    >upgrade your plan to gold</v-card-title
                                  >
                                  <v-card-subtitle>with a new plan</v-card-subtitle>
                                </div>
                              </div>
                            </v-card>
                          </v-col>
                        </v-col>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-col>
              </v-row>
            </v-app>
          </v-layout>
        </v-container>
      </v-app>
    </v-responsive>
  </div>
</template>

<script>
// import { GChart } from "vue-google-charts";
export default {
  data() {
    return {
      chartData: [
        ["Year", "Sales", "Expenses", "Profit"],
        ["2014", 1000, 400, 200],
        ["2015", 1170, 460, 250],
        ["2016", 660, 1120, 300],
        ["2017", 1030, 540, 350],
        ["2018", 1025, 530, 302],
        ["2019", 1040, 560, 356],
      ],
      chartOptions: {
        chart: {
          title: "Company Performance",
          subtitle: "Sales, Expenses, and Profit: 2016-2019",
        },
      },
    };
  },
  computed: {
    theme() {
      return this.$vuetify.theme.dark ? "dark" : "light";
    },
  },
};
</script>
<style scoped>
.rounded {
  border-radius: 30px;
}
.ligne {
  border-right: solid 1px red;
}
</style>

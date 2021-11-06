<template>
  <div>
    <nav>
      <v-navigation-drawer
        v-model="drawer"
        dark
        app
        class="purple"
        expand-on-hover
        permanent
      >
        <v-list>
          <v-list-item
            v-for="link in links"
            :key="link"
            router
            :to="link"
            active-class="border"
          >

            <v-list-item-action>
              <v-icon>{{ link.icon }}</v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>{{ link.text }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </nav>
  </div>
</template>
<i class="fab fa-red-river"></i>
<script>
export default {
  data() {
    return {
      drawer: true,
      links: [
        { icon: "fs fa-home", text: "home", route: "/", color: "green" },
        { icon: "far fa-credit-card", text: "balance", route: "/fahad", color: "green" },
        { icon: "fas fa-chart-line", text: "investments", route: "/footer" },
        { icon: "fas fa-balance-scale-right", text: "insurance", route: "/body" },
        { icon: "fas fa-briefcase", text: "business", route: "/home" },
        { icon: "fas fa-briefcase", text: "business", route: "/home" },
      ],
      ],
      slides: [
        " online check and payment",
        " online check and payment",
        " online check and payment",
        " online check and payment",
      ],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style scoped>
.border {
  border-left: 4px solid black;
}
</style>

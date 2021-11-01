<template>
  <div>
    <Body />

    <Nav />
  </div>
</template>

<script>
import Body from "../components/Body";

import Nav from "../components/Nav";
export default {
  name: "Home",

  components: {
    Body,

    Nav,
  },
};
</script>

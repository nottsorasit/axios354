<template>
  <div class="home">
    <work/>
  </div>
</template>

<script>
// @ is an alias to /src
import work from "@/components/axios.vue";

export default {
  name: "Home",
  components: {
    work
  }
};
</script>

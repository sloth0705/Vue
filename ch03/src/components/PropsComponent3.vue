<script>
import PropsComponent4 from "./PropsComponent4.vue";

export default {
  name: "PropsComponent3",
  props: ["c3Name", "c3Age", "c4Name", "c4Age"],
  components: { PropsComponent4 },
};
</script>
<template>
  <h4>PropsComponent3</h4>
  <p>
    c3Name: {{ c3Name }}<br />
    c3Age: {{ c3Age }}
  </p>
  <PropsComponent4 :c4Name="c4Name" :c4Age="c4Age" />
</template>
<style scoped></style>

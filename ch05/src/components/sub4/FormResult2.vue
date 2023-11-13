<script setup>
import { reactive } from "vue";
import { useRoute } from "vue-router";

// router 인스턴스 가져오기
const router = useRoute();
// router query 데이터 수신
const user = router.params;
</script>
<template>
  <h4>FormResult2</h4>
  <p>name: {{ user.name }}</p>
  <p>age: {{ user.age }}</p>
  <p>addr: {{ user.addr }}</p>
</template>
<style scoped></style>

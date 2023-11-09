<template>
  <h3>Composition API</h3>
  <h4>Reactivity</h4>
  <Component1 />
  <h4>LifeCycle Hooks</h4>
  <Component2 />
  <h4>Dependency Injection</h4>
  <Component3 />
</template>

<script>
/*
  Composition API

  Vue 프로젝트 생성
  - Options API 기반 : npm init vite-app 프로젝트명
  - Composition API 기반 : npm init vite-@latest

*/
import { provide } from "vue";
import Component1 from "./components/Component1.vue";
import Component2 from "./components/Component2.vue";
import Component3 from "./components/Component3.vue";

export default {
  name: "App",
  components: { Component1, Component2, Component3 },
  setup() {
    let user1 = {
      name: "김유신",
      age: 25,
      addr: "김해",
    };
    // App 컴포넌트 하위 컴포넌트에서 inject 주입
    provide("user1", user1);
  },
};
</script>

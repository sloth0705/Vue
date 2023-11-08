<script>
import EmitComponent1 from "./components/EmitComponent1.vue";
import LifeCompoonent from "./components/LifeCompoonent.vue";
import MyComponent1 from "./components/MyComponent1.vue";
import MyComponent2 from "./components/MyComponent2.vue";
import MyComponent3 from "./components/MyComponent3.vue";
import OptionComponent1 from "./components/OptionComponent1.vue";
import OptionComponent2 from "./components/OptionComponent2.vue";
import OptionComponent3 from "./components/OptionComponent3.vue";
import OptionComponent4 from "./components/OptionComponent4.vue";
import PropsComponent1 from "./components/PropsComponent1.Vue";
import PropsComponent2 from "./components/PropsComponent2.vue";
import PropsComponent3 from "./components/PropsComponent3.vue";

export default {
  name: "App",
  data() {
    return {
      cities: ["서울", "대전", "대구", "부산", "광주"],
      isShow: true,
    };
  },
  methods: {
    emitHandler: function (data) {
      console.log(data.name);
      console.log(data.age);
    },
    btnToggle: function () {
      this.isShow = !this.isShow;
    },
  },
  components: {
    MyComponent1,
    MyComponent2,
    MyComponent3,
    OptionComponent1,
    OptionComponent2,
    OptionComponent3,
    OptionComponent4,
    PropsComponent1,
    PropsComponent2,
    PropsComponent3,
    EmitComponent1,
    LifeCompoonent,
  },
};
</script>

<template>
  <h3>Components</h3>
  <h4>컴포넌트</h4>
  <MyComponent1 />
  <MyComponent2 />
  <MyComponent3 />
  <h4>Options API</h4>
  <OptionComponent1 />
  <OptionComponent2 />
  <OptionComponent3 />
  <OptionComponent4 />
  <h4>컴포넌트 통신</h4>
  <PropsComponent1 name="김유신" />
  <PropsComponent1 name="김춘추" age="21" />
  <ul>
    <PropsComponent2 v-for="city in cities" :mycity="city" />
  </ul>
  <PropsComponent3 c3Name="홍길동" c3Age="23" c4Name="강감찬" c4Age="33" />
  <EmitComponent1 name="홍길동" age="12" @myEmit="emitHandler" />
  <h4>컴포넌트 생명주기</h4>
  <LifeCompoonent v-if="isShow" />
  <button @click="btnToggle">토글링</button>
</template>

<style scoped></style>

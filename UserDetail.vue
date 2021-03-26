<template>
  <div>
    <div>
      <h3>UserDetail Page</h3>
      <!-- <p>{{ nameOfChild }}</p> -->
      <p>name :{{ nameOfChild.name }}</p>
      <p>family name :{{ nameOfChild.familyName }}</p>
      <p>child1 test name : {{ nameOfChild1 }}</p>
    </div>
  </div>
</template>

<script>
export default {
  //   props: { nameOfChild: String },
  props: {
    nameOfChild: {
      // name: "asd",
      type: Object,
      default: "G_G_",
    },
    nameOfChild1: String, // child1에 type없이 "name"으로만 들어가면 "name"은 String 이라고 알려주면서 오류 뜸
  },
  //   props: ["nameOfChild"],

  //데이터 타입을 기록하기 위해서 array가 아니라 오브젝트형으로 써줌.
  //값이 들어갈수없는 이유는 부모 컴포넌트에서 이미 값이 상속되었기 때문에  값이아닌 타입이들어감
  data() {
    return {};
  },
};
</script>
<template>
  <div>
    <h1>User Components Page</h1>
    <p>name : {{ name }}</p>
    <v-btn @click="changeName()">changeName</v-btn>
    <hr />
    <UserDetail1
      :nameOfChild="{ name: '이름', familyName: '성' }"
      :nameOfChild1="name"
    ></UserDetail1>
    <div>
      <label for="email">email</label>
      <input type="text" id="email" v-model="email" />
    </div>
    <div>
      <label for="name">성함</label>
      <input type="text" id="name" v-model="name" />
    </div>
    <div>
      <label for="password">비밀번호</label>
      <input type="password" id="password" v-model="password" />
    </div>
    <div>
      <label for="passwordConfirm">비밀번호 확인</label>
      <input type="password" id="passwordConfirm" v-model="passwordConfirm" />
    </div>
    <div>
      <label for="position">직책</label>
      <input type="text" id="position" v-model="position" />
    </div>
    <div>
      <label for="teamName">팀 이름</label>
      <input type="text" id="teamName" v-model="teamName" />
    </div>
    <button type="submit">회원가입</button>
    <!-- <UserEdit></UserEdit> -->
  </div>
</template>

<script>
import UserDetail1 from "./UserDetail.vue";
// import UserEdit from "./component/UserEdit.vue";

export default {
  components: { UserDetail1 },

  data() {
    return {
      name: "Vuevuevue",
    };
  },
  methods: {
    changeName: function () {
      this.name = "이름";
    },
    submitForm() {
      console.log("asd");
    },
  },
};
</script>
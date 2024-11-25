<!--<script setup>-->
<script>
import Header from './components/layout/Header.vue';
import Footer from './components/layout/Footer.vue';

//! options 스타일
export default {
  components: {
      Header,
      Footer
  },
  data() {
    return {
    };
  },
  methods: {
    
  },

  // 자주 사용되는 메모리에 띄워놓기
  computed: {
  },

  // 특정 값을 변경감지한다 기존의 값도 알고, 새로운 값도 알 수 있음
  watch: {
  },

  mounted() {
  }
}
</script>
<template>
  <Header />
  <router-view />
  <Footer />
</template>

<!--scoped 를 붙이면 이 컴포넌트에서만 적용된다, 없으면 다른 파일까지 오염-->
<style>
@import "./assets/scss/common.scss";
/*
외부 스타일 import
@import "./assets/main.css";
@import "@/assets/main.css";
 */
  /* span {
    font-size: 25px;
  } */

</style>

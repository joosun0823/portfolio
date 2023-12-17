<template lang="">
  <div class="skills">
    <h1>2</h1>
    <h3>SKILLS</h3>
    <ul class="skills_list">
      <li><figure><img src="../assets/html.png" alt=""></figure> <span>웹표준, 접근성 준수, 상황에 따라 적절한 태그 사용 </span></li>
      <li><figure><img src="../assets/css.png" alt=""></figure> <span>css3로 프로젝트의 디자인에 알맞은 스타일 적용, 반응형 웹작업 </span></li>
      <li><figure><img src="../assets/js.png" alt=""></figure> <span>ES6 문법의 활용으로 적절한 로직 구현</span></li>
      <li><figure><img src="../assets/sass.png" alt=""></figure> <span>css의 가독성을 높이고 scss문법에 익숙해 용이하게 사용 가능</span></li>
      <li><figure><img src="../assets/jquery.png" alt=""></figure> <span>자바스크립트 라이브러리, DOM 조작 및 이벤트 처리</span></li>
      <li><figure><img src="../assets/git.png" alt=""></figure> <span>Github를 활용하여 프로젝트 관리 및 배포 </span></li>
      <li><figure><img src="../assets/vue.png" alt=""></figure> <span>컴포넌트 기반으로 Store를 사용하며 반응적이고 유연한 UI 구축 </span></li>
      <li><figure><img src="../assets/react.png" alt=""></figure> <span>컴포넌트 기반으로 웹 어플리케이션 개발, JSX를 통한 선언적 UI 작성 가능</span></li>
      <li><figure><img src="../assets/mysql.png" alt=""></figure> <span>오픈소스, 데이터베이스 관리 가능</span></li>
      <li><figure><img src="../assets/mongodb.png" alt=""></figure> <span>json 형태의 데이터 저장, 관리 가능</span></li>
      <li><figure><img src="../assets/next.png" alt=""></figure> <span>컴포넌트 기반으로 반응적이고 유연한 UI 구축</span></li>
      <li><figure><img src="../assets/mariadb.png" alt=""></figure> <span>MySQL과 연결하여 안정적이고 빠른 속도, 복제 기능 구현</span></li>
      <li><figure><img src="../assets/vercel.png" alt=""></figure> <span>Github와 연동하여 서버리스 기능과 함께 웹 어플리케이션 배포 가능</span></li>
      <li><figure><img src="../assets/netlify.png" alt=""></figure> <span>서버리스 기능과 함께 안정적인 웹사이트 배포 가능</span></li>
    </ul>
  </div>
</template>
<script>
import { onMounted } from "@vue/runtime-core";
import AOS from "aos";

export default {
  name:"SkillsVue",
  setup() {
    onMounted(() => {
      AOS.init();
    });
  },
}
</script>
<style lang="scss">
@keyframes slide {
  0% { transform: translateY(0); }
  100% { transform: translateY(-360px); } 
}
  .skills{
    width: 50%;
    text-align: left;
    padding: 120px 0 120px 120px;
    border-left: 1px solid #5a5a5a;
    h1{
      font-size: 120px;
      color: #FFC700;

    }
    h3{
      font-size: 45px;
      margin-bottom: 80px;
    }
    .skills_list{
      height: 800px;
      overflow: auto;
      
      >li{
        list-style: none;
        margin-bottom: 25px;
        display: flex;
        align-items: center;
          // animation: slide 10s infinite;
        >span{
          margin-left: 20px;
        }
      }
    }
  }


@media (min-width: 768px) and (max-width: 1280px) {
  .skills{
    border-left: none;
    border-top: 1px solid  #5a5a5a;
    width: 100%;
    padding:80px 0;
    > h1{
        font-size: 60px;
      }
    > h3{
      font-size: 25px;
    }
  }
}

@media (max-width: 767px){
  .skills{
    border-left: none;
    border-top: 1px solid  #5a5a5a;
    width: 100%;
    padding:40px 0;
    > h1{
        font-size: 40px;
      }
    > h3{
      font-size: 25px;
    }

    .skills_list{
      padding: 0 15px;
      > li{
        font-size: 14px;
      }
    }
  }
}
</style>
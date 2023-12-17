<template lang="">
  <div class="top">
    <h1 data-aos="fade-right" data-aos-duration="1500">
      KIM<br>JOO-SUN
    </h1>
    <a class="download" href="./pdf/김주선-입사지원서.pdf" download="김주선-입사지원서.pdf">
      <figure>
        <img src="../assets/download.png" alt="">
      </figure>
      <span>이력서 다운로드</span>
    </a>
    
  </div>
</template>
<script>
import AOS from "aos";
import { onMounted } from "@vue/runtime-core";

export default {
  name:'TopTitle',
  setup() {
    onMounted(() => {
      AOS.init();
    });
  },
}
</script>
<style lang="scss">
  .top{
    display: flex;
    width: 100%;
    justify-content: space-between;
    border-bottom: 1px solid #5a5a5a;
    >h1{
      font-size: 80px;
      margin: 0 0 15px;
      text-align: left;
    }
    .download{
      display: flex;
      align-items: center;
      margin-top: 140px;
      text-decoration: none;
      color: white;
      figure{
        margin: 0;
      }
    }
    
  }

  @media (min-width: 768px) and (max-width: 1280px) {
    .top{
      >h1{
        font-size: 50px;
      }
    .download{
      margin-top: 80px;
      figure{
      }
    }
    
  }
  }

  @media (max-width: 767px) {
    .top{
      >h1{
        font-size: 2rem;
      }
    .download{
      margin-top: 40px;
      > figure{
        >img{
          width: 70%;
        }
      }
      span{
        font-size: 14px;
      }
    }
    
  }
  }
</style>
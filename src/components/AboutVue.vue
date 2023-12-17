<template lang="">
  <div class="about">
      <h1>1</h1>
      <h3>ABOUT</h3>
      <figure data-aos="flip-up" data-aos-duration="1000"><img src="../assets/kjs.jpeg" alt=""></figure>
      <p class="about_name"><span>김주선</span> / <span class="birth">2000.08.23</span></p>
      <p class="about_introduce">
        저는 신입 개발자입니다. 그러기에 아직 배울 점이 많습니다. <br> 
        젊은 피를 가지고 있는만큼 밝은 마음으로 계속해서 공부하여 <br> 
        목표를 이룰 때까지 쭉 달리며 모든 문제에 덤벼보려 합니다. <br> 
        우리 모두가 만족하는 개발자가 되겠습니다.
      </p>
      <ul class="about_contact">
        <li><figure><img src="../assets/email.png" alt=""></figure><span>joosun0823@naver.com</span></li>
        <li><figure><img src="../assets/call.png" alt=""></figure><span>010-4047-5420</span></li>
        <li><figure><img src="../assets/map.png" alt=""></figure><span>서울시 강남구</span></li>
      </ul>
  </div>
</template>
<script>
import { onMounted } from "@vue/runtime-core";
import AOS from "aos";

export default {
  name:'AboutVue',
  setup() {
    onMounted(() => {
      AOS.init();
    });
  },
}
</script>
<style lang="scss">
  .about{
    width: 50%;
    text-align: left;
    padding: 120px 120px 120px 0;
      >h1{
        font-size: 120px;
        color: #FFC700;
      }
      >h3{
        font-size: 45px;
        margin-bottom: 80px;
      }
      >figure{
        width: 100%;
        >img{
          width: 50%;
        }
      }
      .about_name{
        font-size: 40px;
        margin: 60px 0 23px 0;
        .birth{
          font-weight: 100;
        }
      }
      .about_introduce{
        margin-bottom: 80px;
        font-size: 20px;
        line-height: 40px;
        font-weight: 200;
        color:#CCCCCC;
      }
      .about_contact{
        >li{
          list-style: none;
          margin-bottom: 20px;
          display: flex;
          >span{
            margin-left: 30px;
            color:#CCCCCC;
            font-weight: 200;
          }
        }
      }
    
  }

  @media (min-width: 768px) and (max-width: 1280px) {
    .about{
      width: 100%;
      padding: 80px 0;
      > h1{
        font-size: 60px;
      }
      > h3{
        font-size: 25px;
      }
      .about_introduce{
        font-size: 16px;

        br{
          display: none;
        }
      }


      .about_name{
        font-size: 28px;
      }
    }

  }


  @media (max-width: 767px){
    .about{
      width: 100%;
      padding: 40px 0;
      > h1{
        font-size: 40px;
      }
      > h3{
        font-size: 25px;
      }
      .about_introduce{
        font-size: 14px;

        br{
          display: none;
        }
      }
      .about_name{
        font-size: 25px;
      }
    }

  }
</style>
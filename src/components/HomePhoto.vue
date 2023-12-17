<template lang="">
    <div class="background">
      <div class="main">
        <h1>프론트엔드 포트폴리오</h1>
        <h3>밝고 명랑한 신입 웹 개발자 김주선입니다.</h3>
      </div>
      <figure class="scroll_button" @click="viewScroll" ><img src="../assets/scroll_button.png" alt=""></figure>
    </div>
</template>
<script>
export default {
  name:'HomePhoto',
  methods: {
    viewScroll(){
      window.scrollTo({
        left:0,
        top:935,
        behavior:'smooth'
      })
    }
  },
  mounted(){
    //window.addEventListener('scroll',this.viewScroll)
      
  },
  unmounted(){
    //window.removeEventListener('scroll',this.viewScroll)
  },
}
</script>
<style lang="scss">
@keyframes button_ani {
  0%{
    transform: translateY(0%);
  }

  50%{
    transform: translateY(-30%);
  }

  100%{
    transform: translateY(0%);
  }
}


.background{
  width: 100%;
  height: 100vh;
  background-image: url(../assets/code.jpg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  border-bottom: 1px solid white;
  &::after{ 
    content: '';
    left: 0;
    right: 0;
    bottom: 0;
    top: 0;
    background: #000000;
    opacity: 0.7;
    position: absolute;
    height: 100vh;
  }

  .main{
      width: 100%;
      position: absolute;
      top: 50%;
      left: 0;
      -webkit-transform: translate(0, -50%);
      -ms-transform: translate(0, -50%);
      transform: translate(0, -50%);
      z-index: 100;
      >h1{     
        border-top: 3px solid;
        width: 25%;
        border-bottom: 3px solid;
        padding: 55px 0px;
        text-align: center;
        margin: 0 auto;
        color: white; 
        font-size: 45px;
      }
      >h3{
        color: #a0a0a0;
        margin-top: 200px;
        font-size: 25px;
        font-weight: 400;
      } 
  }

  .scroll_button{
        margin: 0;
        position: absolute;
        bottom: 8%;
        right: 0;
        left: 0;
        z-index: 100;
        animation: button_ani 2s infinite;
      }
}



@media (min-width: 768px) and (max-width: 1280px) {
  .background{
    .main{
      > h1{
        font-size: 2rem;
      }
      >h3{
        font-size: 1.5rem;
      }
    }
  }
}


@media (max-width: 767px) {
  .background{
    .main{
      > h1{
        font-size: 1.3rem;
      }
      >h3{
        font-size: 1rem;
      }
    }

    .scroll_button{
      > img {
        width: 5%;
      }
    }
  }
}




</style>
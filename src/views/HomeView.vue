<template>
  <div class="home">
    <HomePhoto/>
  </div>
  <div class="main_content">
    <TopTitle/>
    <div class="onetwo"> 
      <AboutVue/>
      <SkillsVue/>
    </div>
    <WorkVue/>
    <ProjectsVue/>
    <ContactVue/>
  </div>


  <div class="fixed_button" v-if="showTopButton" @click="scrollToTop"  data-aos="zoom-in">
    <figure>
      <img src="../assets/top_button.png" alt="">
    </figure>
  </div>
</template>

<script>
// @ is an alias to /src
import HomePhoto from '@/components/HomePhoto.vue';
import TopTitle from '@/components/TopTitle.vue';
import AboutVue from '@/components/AboutVue.vue'
import SkillsVue from '@/components/SkillsVue.vue'
import ProjectsVue from '@/components/ProjectsVue.vue';
import ContactVue from '@/components/ContactVue.vue';
import WorkVue from '@/components/WorkVue.vue';
import AOS from "aos";
import { onMounted } from "@vue/runtime-core";



export default {
  name: 'HomeView',
  components: {
    HomePhoto,
    TopTitle,
    AboutVue,
    SkillsVue,
    ProjectsVue,
    ContactVue,
    WorkVue
  },
  data(){
    
    return{
      showTopButton: false
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
    
  },
  unmounted() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.scrollY > 500) {
        this.showTopButton = true;
      } else {
        this.showTopButton = false;
      }
    },
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    }
  },
  setup() {
    onMounted(() => {
      AOS.init();
    });
  },
}
</script>

<style lang="scss">
.main_content{
  padding: 160px 180px 120px;
  .onetwo{
    width: 100%;
    display: flex;
  }
}

.fixed_button{
  position: fixed;
  bottom: 10%;
  right: 2%;
  width: 60px;
  height: 60px;
  
  border: none;
  border-radius: 50%;
  background-color: #FFC700;
  display: flex;
      justify-content: center;
      align-items: center;
  > figure{
    width: 60px;

    > img{

      }
  }
      
    // > button{
      

    //   margin-bottom: 25px;
    //   color: black;
      
    // }
  
}



@media (min-width: 768px) and (max-width: 1280px){
  .main_content{
    padding: 140px 140px 120px;

    .onetwo{
      flex-direction: column;
    }
  }

}

@media (max-width: 767px) {
  .main_content{
    padding: 20px 30px 20px;

    .onetwo{
      flex-direction: column;
    }
  }
  .fixed_button{
    width: 50px;
    height: 50px;
    > figure{
      img{
        width: 50%;
      }
    }
  }
}

</style>
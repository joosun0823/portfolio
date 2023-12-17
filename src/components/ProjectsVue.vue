<template lang="">
  <div class="projects">
    <div class="projects_title">
      <div class="title_name">
      <h1>4</h1>
      <h3>PROJECTS</h3>
    </div>
      <p>
        배운 기술들을 이용해 평소에 <br>
        해보고 싶었던 주제의 프로젝트로<br>
        경험을 쌓아보았습니다.
      </p>
    </div>
    <div class="projects_list">
      <ul>
        <li data-aos="fade-left" data-aos-duration="1500">
          <figure>
            <img src="../assets/everland.png" alt="">
          </figure>
          <div>
            <span class="date">2023.09</span>
            <h2>에버랜드 사이트 리뉴얼</h2>
            <p>
              카드할인 정보, 즐길거리 등 모두 data.json으로 데이터화 <br> 
              시켜 불러오고, 팝업 형식의 상세 페이지
            </p>
            <span class="tool">HTML, SCSS, JAVASCRIPT, SWIPER, GITHUB</span>
            <div class="git_button">
              <a href="https://github.com/joosun0823/everland.git" target="_blank"><button><img src="../assets/git_button.png"> Github </button></a>
              <a href="https://joosun0823.github.io/everland/" target="_blank"><button><img src="../assets/desktop.png">View</button></a>
            </div>
          </div>
        </li>
        <li data-aos="fade-left" data-aos-duration="1500">
          <figure>
            <img src="../assets/worldcup.png" alt="">
          </figure>
          <div>
            <span class="date">2023.10</span>
            <h2>이상형 월드컵 어플</h2>
            <p>
              React.js와 data.json으로 연예인들 목록, 동물 목록 등 <br>
              직접 데이터화 시켜 만든 이상형 월드컵 모바일 웹
            </p>
            <span class="tool">REACT, SCSS, GITHUB</span>
            <div class="git_button">
              <a href="https://github.com/joosun0823/react-project.git" target="_blank"><button><img src="../assets/git_button.png" target="_blank"> Github </button></a>
              <a href="https://joosun0823.github.io/react-project/" target="_blank"><button><img src="../assets/desktop.png">View</button></a>
            </div>
          </div>
        </li>
        <li data-aos="fade-left" data-aos-duration="1500">
          <figure>
            <img src="../assets/saju.png" alt="">
          </figure>
          <div>
            <span class="date">2023.10</span>
            <h2>별별연인</h2>
            <p>
              AI 검색엔진 api를 이용한 사주 연애매칭 어플 
            </p>
            <span>
              본인과 어울리는 오행을 가진 사람들 목록  <br>
              불러오는 기능 구현
            </span>
            <span class="tool">NEXT, SCSS, SWIPER, VERCEL</span>
            <div class="git_button">
              <a href="https://github.com/joosun0823/next-b3o2.git" target="_blank"><button><img src="../assets/git_button.png"> Github </button></a>
              <a href="https://next-b3o2.vercel.app/" target="_blank"><button><img src="../assets/desktop.png">View</button></a>
            </div>
          </div>
        </li>
        <li data-aos="fade-left" data-aos-duration="1500">
          <figure>
            <img src="../assets/portfolio.png" alt="">
          </figure>
          <div>
            <span class="date">2023.11</span>
            <h2>포트폴리오</h2>
            <p>
              Vue.js를 이용하여 만든 자기소개 프로젝트
            </p>
            <span class="tool">VUE, CSS, GITHUB, NETLIFY</span>
            <div class="git_button">
              <a href="https://github.com/joosun0823/portfolio.git" target="_blank"><button><img src="../assets/git_button.png"> Github </button></a>
              <a href="https://shiny-narwhal-a412e7.netlify.app" target="_blank"><button><img src="../assets/desktop.png">View</button></a>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
import { onMounted } from "@vue/runtime-core";
import AOS from "aos";

export default {
  name:'ProjectsVue',
  setup() {
    onMounted(() => {
      AOS.init();
    });
  },
}
</script>
<style lang="scss">
  .projects{
    padding-top: 100px;
    padding-bottom: 60px;
    border-top: 1px solid #5a5a5a;
    display: flex;
    .projects_title{
      .title_name{
            >h1{
            font-size: 120px;
            color: #FFC700;
            text-align: left;
          }
          >h3{
            font-size: 45px;
            margin-bottom: 65px;
            text-align: left;
          }
      }
      
      >p{
        text-align: left;
        line-height: 40px;
        font-weight: 200;
        color: #CCCCCC;
        font-size: 20px;

      }
    }
    .projects_list{
      margin-left: 200px;
      >ul{
        >li{
          display: flex;
          align-items: center;
          border-bottom:  1px solid #5a5a5a ;
          padding: 60px;
          &:nth-of-type(4){
            border: none;
          }
          > div{
            text-align: left;
            margin-left: 150px;
            

            .date, p, span, .tool{
              font-size: 20px;
              color: #CCCCCC;
              font-weight: 200;
              line-height: 40px;
            }

            .date{
              
            }
            h2{
              font-size: 40px;
              font-weight: 400;
              margin-bottom: 10px;
            }
            p{
              margin-bottom: 20px;
            }
            span{
              display: block;
              margin-bottom: 10px;

            }
            .tool{
              font-size: 16px;
              color: #999999;
            }

            .git_button{
              margin-top: 15px;
              display: flex;
              gap: 20px;
              > a > button{
              width: 120px;
              height: 40px;
              display: flex;
              align-items: center;
              justify-content: center;
              font-size: 18px;
              gap: 5px;
              font-weight: bold;
              border-radius: 30px;
              background-color: #FFC700;
              border: none;
              cursor: pointer;
              }
            }
            
          }
          
        }
      }
    }
  }


  @media (min-width: 768px) and (max-width: 1280px) {

    .projects{
      padding-top: 80px;
      flex-direction: column;
      .projects_title{
        display: flex;  
        margin-bottom:100px;
        .title_name{
          > h1{
        font-size: 60px;
          }
          > h3{
        font-size: 25px;
            margin-bottom: 0;
          }
        }
        >p{
          display: flex;
          align-items: center;
          margin-left: 180px; 
          font-size: 16px;

          >br{
            display: none;
          }

        }
      }

      .projects_list{
        margin-left: 0;
        > ul{
          >li{
            padding: 60px 0;
            > div{  
              margin-left:70px;
              h2{
                font-size: 25px;
              }
              >span{
                font-size: 16px;
              }
              >p{
                font-size: 16px;

                >br{
                  display: none;
                }
              }


              .git_button{
              margin-top: 15px;
              display: flex;
              gap: 20px;
              > a > button{
              width: 100px;
              height: 40px;
              font-size: 14px;
              &:nth-of-type(1){
                width: 120px;
              }
              }
            }
            
            }
          }
        }
      }
    }
  }

  @media (max-width: 767px) {
    .projects{
      padding-top: 40px;
      flex-direction: column;
      .projects_title{
        display: flex;  
        margin-bottom:40px;
        .title_name{
          > h1{
        font-size: 40px;
          }
          > h3{
        font-size: 25px;
            margin-bottom: 0;
          }
        }
        >p{
          display: flex;
          align-items: center;
          margin-left: 80px; 
          font-size: 14px;

          >br{
            display: none;
          }

        }
      }

      .projects_list{
        margin-left: 0;
        > ul{
          >li{
            flex-direction: column;
            padding: 40px 0;
            > div{  
              padding: 30px 50px;
              margin: 0;
              h2{
                font-size: 20px;
              }
              >span{
                font-size: 14px;
              }
              >p{
                font-size: 14px;

                >br{
                  display: none;
                }
              }


              .git_button{
              margin-top: 15px;
              display: flex;
              gap: 20px;
              > a > button{
              width: 100px;
              height: 40px;
              font-size: 14px;
              &:nth-of-type(1){
                width: 120px;
              }
              }
            }
            
            }
          }
        }
      }
    }
  }
</style>
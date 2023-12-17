<template lang="">
  <div class="work">
    <div class="work_title">
      <div class="work_name">
      <h1>3</h1>
      <h3>WORK</h3>
    </div>
      <p>
        배운 기술들을 활용해 <br>
        연습 겸 공부해 본 작업물입니다.
      </p>
    </div>
    <div class="work_list">
      <ul>
        <li data-aos="fade-left" data-aos-duration="1500">
          <figure>
            <img src="../assets/bing.png" alt="">
          </figure>
          <div>
            <span class="date">2023.06</span>
            <h2>빙그레 사이트 클론코딩</h2>
            <p>
              코딩을 시작하며 처음 구현해 본 클론 사이트 <br>
              메인페이지, 회사소개, 제품소개 페이지 구현
            </p>
            <div class="inform">
              <span class="tool">HTML, SCSS, SWIPER, GITHUB</span>
              <div class="git_button">
                <a href="https://github.com/joosun0823/clone.git" target="_blank"><button><img src="../assets/git_button.png"> Github </button></a>
                <a href="https://joosun0823.github.io/clone/" target="_blank"><button><img src="../assets/desktop.png">View</button></a>
              </div>
            </div>
          </div>
        </li>
        <li data-aos="fade-left" data-aos-duration="1500">
          <figure>
            <img src="../assets/movie.png" alt="">
          </figure>
          <div>
            <span class="date">2023.7</span>
            <h2>MovieAPI 데이터 불러오기</h2>
            <p>
              API key를 이용하여 영화 데이터들을 불러들인 작업<br>
              자세히 보기 버튼을 눌러 상세페이지까지 나오는 기능 구현
            </p>
            <div class="inform">
              <span class="tool">REACT, SCSS, GITHUB</span>
              <div class="git_button">
                <a href="https://github.com/joosun0823/movie.git" target="_blank"><button><img src="../assets/git_button.png" target="_blank"> Github </button></a>
                <a href="https://movie-indol-gamma.vercel.app/" target="_blank"><button><img src="../assets/desktop.png">View</button></a>
              </div>
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
  name:'WorkVue',
  setup() {
    onMounted(() => {
      AOS.init();
    });
  },
}
</script>
<style lang="scss">
  .work{
    padding-top: 100px;
    padding-bottom: 60px;
    border-top: 1px solid #5a5a5a;
    display: flex;
    .work_title{
      .work_name{
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
    .work_list{
      margin-left: 250px;
      >ul{
        >li{
          border-bottom:  1px solid #5a5a5a ;
          padding: 60px;
          &:nth-of-type(2){
            border: none;
          }
          > figure{
            img{
              width: 100%;
            }
          }

          > div{
            text-align: left;
            margin-top: 30px;
            

            .date, p, span, .tool{
              font-size: 20px;
              color: #CCCCCC;
              font-weight: 200;
              line-height: 40px;
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
            .inform{
              display: flex;
              align-items: center;
              justify-content: space-between;
              margin-top: 20px;
              .tool{
                font-size: 16px;
                color: #999999;
                margin: 0;
              }
  
              .git_button{
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
  }


  @media (min-width: 768px) and (max-width: 1280px) {

    .work{
      padding-top: 80px;
      flex-direction: column;
      .work_title{
        display: flex;  
        margin-bottom:100px;
        .work_name{
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

      .work_list{
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


              }

            .inform{
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
  }

  @media (max-width: 767px) {
    .work{
      padding-top: 40px;
      flex-direction: column;
      .work_title{
        display: flex;  
        margin-bottom:40px;
        .work_name{
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

      .work_list{
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


              }

              .inform{
                display: block;
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
  }
</style>
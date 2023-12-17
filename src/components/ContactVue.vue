<template lang="">
  <div class="contact">
    <div class="contact_title">
      <div class="title_name">
      <h1>5</h1>
      <h3>CONTACT</h3>
      </div>
      <p>
        전 준비되있습니다. <br>
        궁금한 점이 있으시다면 <br>
        언제든지 풀어드리겠습니다.
      </p>
    </div>
    <div class="contact_form" data-aos="zoom-in" data-aos-duration="1000">
      <form class="contact_inform" 
      ref="form"
      @submit.prevent = "sendEmail"
      >
        <input type="text" id="name" name="name" placeholder="NAME"/>
        <input type="text" id="email" name="email" placeholder="EMAIL"/>
        <input type="text" id="phone" name="phone" placeholder="PHONE NO.">
        <textarea name="message" id="message" cols="30" rows="10" placeholder="MESSAGE"></textarea>
        <input type="submit" value="SEND" class="form_submit" />
      </form>
    </div>
  </div>
</template>

<script>
import emailjs from '@emailjs/browser'
import { onMounted } from "@vue/runtime-core";
import AOS from "aos";

export default {
  name: 'ContactVue',
  methods: {
    sendEmail() {
      const name = this.$refs.form.name.value.trim();
      const email = this.$refs.form.email.value.trim();
      const phone = this.$refs.form.phone.value.trim();
      const message = this.$refs.form.message.value.trim();


      if (!name || !email || !phone || !message) {
        alert('빈칸을 모두 채워주세요');
      } else {
        emailjs.sendForm('service_rgneiwa', 'template_hofjtvw', this.$refs.form, 'OKdOM76yr5dVydFXo')
          .then((result) => {
            console.log('SUCCESS!', result.text);
            alert('전송되었습니다');
            this.reloadPage();
          }, (error) => {
            console.log('FAILED...', error.text);
          });
      }
    },
    reloadPage() {
      window.location.reload();
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
.contact {
  border-top: 1px solid #5a5a5a;
  padding-top: 100px;
  display: flex;

  .contact_title {
    .title_name {
      >h1 {
        font-size: 120px;
        color: #FFC700;
        text-align: left;
      }

      >h3 {
        font-size: 45px;
        margin-bottom: 65px;
        text-align: left;
      }
    }

    >p {
      text-align: left;
      line-height: 40px;
      font-weight: 200;
      color: #CCCCCC;
      font-size: 20px;
    }

  }

  .contact_form {
    margin-left: 350px;

    .contact_inform {
      margin-top: 50px;

      input {
        width: 700px;
        height: 48px;
        display: block;
        box-sizing: border-box;
        border: 1px solid #8E8E8E;
        background-color: transparent;
        margin-bottom: 20px;
        color: white;
        padding-left: 16px;
      }

      textarea {
        width: 700px;
        height: 200px;
        padding-top: 15px;
        padding-left: 16px;
        background-color: transparent;
        color: white;
        box-sizing: border-box;
        resize: none;
        margin-bottom: 20px;

        &::placeholder {
          position: absolute;
          top: 15px;
          left: 16px;
          font-family: inherit;
        }
      }

      .form_submit {
        border: none;
        background-color: #FFC700;
        color: black;

        &:hover {
          cursor: pointer;
        }
      }
    }
  }
}

@media (min-width: 768px) and (max-width: 1280px) {
  .contact {
    flex-direction: column;

    .contact_title {
      display: flex;
      margin-bottom: 100px;

      .title_name {

        >h1 {
          font-size: 60px;
        }

        >h3 {
          margin-bottom: 0;
          font-size: 25px;

        }
      }

      >p {
        display: flex;
        align-items: center;
        margin-left: 180px;
        font-size: 16px;
        >br {
          display: none;
        }

      }
    }

    .contact_form {
      margin: 0 auto;

      .contact_inform {
        width: 500px;

        input {
          width: 500px;
          height: 40px;
        }

        textarea {
          width: 500px;
        }

        .form_submit {}
      }
    }
  }
}



@media (max-width: 767px){

  .contact {
    flex-direction: column;

    .contact_title {
      display: flex;
      margin-bottom: 100px;

      .title_name {

        >h1 {
          font-size: 60px;
        }

        >h3 {
          margin-bottom: 0;
          font-size: 25px;

        }
      }

      >p {
        display: flex;
        align-items: center;
        margin-left: 80px;
        font-size: 14px;
        >br {
          display: none;
        }

      }
    }

    .contact_form {
      margin: 0 auto;

      .contact_inform {
        width: 300px;

        input {
          width: 300px;
          height: 40px;
        }

        textarea {
          width: 300px;
        }

        .form_submit {}
      }
    }
  }
}
</style>
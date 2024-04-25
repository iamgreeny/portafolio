<script setup>
import SocialLinks from "@/components/layouts/SocialLinks.vue";
import { ref } from "vue";
import emailjs from "@emailjs/browser";

const form = ref({
  name: "",
  email: "",
  message: "",
});

const handleSubmit = () => {
  console.log("Form:", form.value);
  console.log(emailjs);
  let serviceID = "service_4xhmpxm";
  let templateID = "template_ht27ilh";
  let publicKey = "P-zDHtrbad0HQ9_5w";
  let templateParams = {
    to_name: form.value.name,
    from_name: form.value.email,
    message: form.value.message,
  };

  emailjs.send(serviceID, templateID, templateParams, publicKey).then(
    (response) => {
      console.log("SUCCESS!", response.status, response.text);
      alert("Message Sent!");
    },
    (err) => {
      console.log("FAILED...", err);
    }
  );
};
</script>

<template>
  <section class="cont_papa">
    <h1>¡BIENVENIDO A MI MUNDO DE COLORES!</h1>
    <form class="form_cont" @submit.prevent="handleSubmit">
      <div class="outer">
        <div class="inner">
          <input type="text" placeholder="Name" v-model="form.name" />
        </div>
      </div>
      <div class="outer">
        <div class="inner">
          <input type="email" placeholder="Email" v-model="form.email" />
        </div>
      </div>
      <div class="outer textarea_outer">
        <div class="inner textarea_inner">
          <textarea
            name=""
            id=""
            cols="30"
            rows="8"
            placeholder="Message"
            v-model="form.message"
          ></textarea>
        </div>
      </div>
      <button type="submit" class="outer">Send</button>
    </form>
    <SocialLinks style="display: none" />
    <img src="/images/contact/tortuga.svg" alt="" />
    <!-- aqui va la imagen nubestortuga-->
  </section>
</template>

<style scoped>
.cont_papa {
  display: flex;
  align-items: center;
  flex-direction: column;
  padding-bottom: 50rem;
}

img {
  position: absolute;
  bottom: 0;
  z-index: -1;
}

h1 {
  display: flex;
  justify-content: center;
  margin-top: 7%;
  font-family: morvem_font;
  color: var(--color-primary);
  text-transform: uppercase;
  font-weight: 100;
  text-align: center;
  font-size: 6rem;
}

.form_cont {
  display: flex;
  flex-direction: column;
  width: 50%;
  gap: 20px;
  margin-top: 4%;
}

.outer {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #efefef;
  height: 100px;
  border-radius: 40px;
  box-shadow: 5px 5px black;
}

.inner {
  background-color: #e27fa6;
  height: 80px;
  width: 95%;
  border-radius: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
}

button {
  font-size: 2rem;
  font-family: gilroy_regular;
  cursor: pointer;
}

.textarea_inner,
.textarea_outer {
  height: max-content;
  padding: 1rem 0rem;
}

input,
textarea {
  border: none;
  background-color: transparent;
  width: 90%;
  height: 90%;
  font-size: 2rem;
  font-family: gilroy_regular;
  color: var(--color-primary);
  text-align: center;
}

::placeholder {
  color: rgb(225, 218, 221);
  opacity: 1; /* Firefox */
}

input:focus,
textarea:focus {
  outline: none;
}

@media only screen and (max-width: 1000px) {
  .form_cont {
    width: 80%;
  }
}

@media only screen and (max-width: 768px) {
  .form_cont {
    width: 80%;
  }
}

@media only screen and (max-width: 600px) {
  .form_cont {
    width: 80%;
  }
  h1 {
    font-size: 4rem;
  }
}

@media only screen and (max-width: 500px) {
  .form_cont {
    width: 80%;
  }

  .inner {
    height: 40px;
    border-radius: 30px;
  }

  .outer {
    height: 50px;
    border-radius: 40px;
  }

  h1 {
    font-size: 2.5rem;
  }

  .cont_papa {
    padding-bottom: 20rem;
  }

  .textarea_inner,
  .textarea_outer {
    height: max-content;
    padding: 1rem 0rem;
  }
}

@media only screen and (max-width: 480px) {
  h1 {
    font-size: 2.2rem;
  }
}

input,
textarea {
  font-size: 1.2rem;
}

button {
  font-size: 1.2rem;
}

@media only screen and (max-width: 360px) {
  h1 {
    font-size: 1.5rem;
  }
}
</style>

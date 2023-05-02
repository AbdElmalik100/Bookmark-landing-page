<template>
  <main>
    <HeaderNav></HeaderNav>
    <div class="landing py-5">
      <div class="container d-flex align-items-center gap-5 flex-column-reverse flex-lg-row">
        <div class="info">
          <h1 class="mb-0">A Simple Bookmark Manager</h1>
          <p class="my-4">
            A clean and simple interface to organize your favourite websites. Open a new browser tab and see your sites
            load
            instantly. Try it for free.
          </p>
          <div class="buttons d-flex align-items-center gap-3">
            <button class="butn">Get it on Chrome</button>
            <button class="butn">Get it on Firefox</button>
          </div>
        </div>
        <div class="hero position-relative">
          <img src="/images/illustration-hero.svg" alt="">
        </div>
      </div>
    </div>
    <div class="features py-5">
      <div class="container">
        <div class="heading w-50 mb-5 m-auto text-center">
          <h1 class="mb-3">Features</h1>
          <p class="mb-0">
            Our aim is to make it quick and easy for you to access your favourite websites. Your bookmarks sync between
            your
            devices so you can access them on the go.
          </p>
        </div>
        <div class="tabs-butns mb-4 pb-4 w-75 mx-auto d-flex align-items-center justify-content-center text-center">
          <span :class="`tab d-block w-50 py-3 ${activeTab === 'tab-1' ? 'active active-one' : ''}`"
            @click="activeTab = 'tab-1'">Simple Bookmarking</span>
          <span :class="`tab d-block w-50 py-3 ${activeTab === 'tab-2' ? 'active active-two' : ''}`"
            @click="activeTab = 'tab-2'">Speedy Searching</span>
          <span :class="`tab d-block w-50 py-3 ${activeTab === 'tab-3' ? 'active active-three' : ''}`"
            @click="activeTab = 'tab-3'">Easy Sharing</span>
          <span class="slider"></span>
        </div>
        <div class="tabs-info mt-5">
          <transition-group type="transition" name="list">
            <div :class="`tabbing tab-one d-flex align-items-center gap-5 ${activeTab === 'tab-1' ? 'active' : ''}`"
              v-if="activeTab === 'tab-1'">
              <div class="feature position-relative">
                <img src="/images/illustration-features-tab-1.svg" alt="">
              </div>
              <div class="details w-75">
                <h2 class="mb-0">Bookmark</h2>
                <p class="my-4">
                  Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control
                  over how you manage your favourite sites.
                </p>
                <button class="butn">More Info</button>
              </div>
            </div>
            <div :class="`tabbing tab-two d-flex align-items-center gap-5 ${activeTab === 'tab-2' ? 'active' : ''}`"
              v-if="activeTab === 'tab-2'">
              <div class="feature position-relative">
                <img src="/images/illustration-features-tab-2.svg" alt="">
              </div>
              <div class="details w-75">
                <h2 class="mb-0">Intelligent search</h2>
                <p class="my-4">
                  Our powerful search feature will help you find saved sites in no time at all. No need to trawl through
                  all
                  of your bookmarks.
                </p>
                <button class="butn">More Info</button>
              </div>
            </div>
            <div :class="`tabbing tab-three d-flex align-items-center gap-5 ${activeTab === 'tab-3' ? 'active' : ''}`"
              v-if="activeTab === 'tab-3'">
              <div class="feature position-relative">
                <img src="/images/illustration-features-tab-3.svg" alt="">
              </div>
              <div class="details w-75">
                <h2 class="mb-0">Share your bookmarks</h2>
                <p class="my-4">
                  Easily share your bookmarks and collections with others. Create a shareable link that you can send at
                  the
                  click of a button.
                </p>
                <button class="butn">More Info</button>
              </div>
            </div>
          </transition-group>
        </div>
      </div>
    </div>
    <div class="extensions py-5 mt-5">
      <div class="container">
        <div class="heading text-center mb-5 w-50 mx-auto">
          <h1 class="mb-3">Download the extension</h1>
          <p class="mb-0">
            We’ve got more browsers in the pipeline. Please do let us know if you’ve got a favourite you’d like us to
            prioritize.
          </p>
        </div>
        <div class="cards mt-5 pt-5">
          <div class="row justify-content-center">
            <div class="col-lg-3 box">
              <div class="extension-card overflow-hidden d-flex flex-column align-items-center gap-2 rounded-4">
                <div class="p-4 text-center">
                  <div class="icon-cont">
                    <img width="100" src="/images/logo-chrome.svg" alt="">
                  </div>
                  <h4 class="mt-4 mb-1">Add to Chrome</h4>
                  <span>Minimum version 62</span>
                </div>
                <img class="dots" src="/images/bg-dots.svg" alt="">
                <div class="p-4 w-100">
                  <button class="butn w-100">Add & Install Extension</button>
                </div>
              </div>
            </div>
            <div class="col-lg-3 box">
              <div class="extension-card overflow-hidden d-flex flex-column align-items-center gap-2 rounded-4">
                <div class="p-4 text-center">
                  <div class="icon-cont">
                    <img width="100" src="/images/logo-firefox.svg" alt="">
                  </div>
                  <h4 class="mt-4 mb-1">Add to Firefox</h4>
                  <span>Minimum version 55</span>
                </div>
                <img class="dots" src="/images/bg-dots.svg" alt="">
                <div class="p-4 w-100">
                  <button class="butn w-100">Add & Install Extension</button>
                </div>
              </div>
            </div>
            <div class="col-lg-3 box">
              <div class="extension-card overflow-hidden d-flex flex-column align-items-center gap-2 rounded-4">
                <div class="p-4 text-center">
                  <div class="icon-cont">
                    <img width="100" src="/images/logo-opera.svg" alt="">
                  </div>
                  <h4 class="mt-4 mb-1">Add to Opera</h4>
                  <span>Minimum version 46</span>
                </div>
                <img class="dots" src="/images/bg-dots.svg" alt="">
                <div class="p-4 w-100">
                  <button class="butn w-100">Add & Install Extension</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="faq py-5">
      <div class="container">
        <div class="heading text-center mb-5 w-50 mx-auto">
          <h1 class="mb-3">Frequently Asked Questions</h1>
          <p class="mb-0">
            Here are some of our FAQs. If you have any other questions you’d like answered please feel free to email us.
          </p>
        </div>
        <div class="questions py-5 w-50 mx-auto">
          <div :class="`quest p-4 ${questOne ? 'active' : ''}`" @click="questOne = !questOne">
            <div class="d-flex align-items-center justify-content-between">
              <h4 class="mb-0">What is Bookmark?</h4>
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="12">
                <path fill="none" stroke="#5267DF" stroke-width="3" d="M1 1l8 8 8-8" />
              </svg>
            </div>
            <div :class="`quest-cont overflow-hidden ${questOne ? 'active' : ''}`">
              <p class="mb-0 mt-3">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce tincidunt justo eget ultricies fringilla.
                Phasellus blandit ipsum quis quam ornare mattis.
              </p>
            </div>
          </div>
          <div :class="`quest p-4 ${questTwo ? 'active' : ''}`" @click="questTwo = !questTwo">
            <div class="d-flex align-items-center justify-content-between">
              <h4 class="mb-0">How can i request a new bowser?</h4>
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="12">
                <path fill="none" stroke="#5267DF" stroke-width="3" d="M1 1l8 8 8-8" />
              </svg>
            </div>
            <div :class="`quest-cont overflow-hidden ${questTwo ? 'active' : ''}`">
              <p class="mb-0 mt-3">
                Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula. Suspendisse
                imperdiet. Vivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non ligula.
                Suspendisse imperdie tVivamus luctus eros aliquet convallis ultricies. Mauris augue massa, ultricies non
                ligula. Suspendisse imperdiet.
              </p>
            </div>
          </div>
          <div :class="`quest p-4 ${questThree ? 'active' : ''}`" @click="questThree = !questThree">
            <div class="d-flex align-items-center justify-content-between">
              <h4 class="mb-0">Is there a mobile app?</h4>
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="12">
                <path fill="none" stroke="#5267DF" stroke-width="3" d="M1 1l8 8 8-8" />
              </svg>
            </div>
            <div :class="`quest-cont overflow-hidden ${questThree ? 'active' : ''}`">
              <p class="mb-0 mt-3">
                Sed consectetur quam id neque fermentum accumsan. Praesent luctus vestibulum dolor, ut condimentum urna
                vulputate eget. Cras in ligula quis est pharetra mattis sit amet pharetra purus. Sed sollicitudin ex et
                ultricies bibendum.
              </p>
            </div>
          </div>
          <div :class="`quest p-4 ${questFour ? 'active' : ''}`" @click="questFour = !questFour">
            <div class="d-flex align-items-center justify-content-between">
              <h4 class="mb-0">What about other Chromium browsers?</h4>
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="12">
                <path fill="none" stroke="#5267DF" stroke-width="3" d="M1 1l8 8 8-8" />
              </svg>
            </div>
            <div :class="`quest-cont overflow-hidden ${questFour ? 'active' : ''}`">
              <p class="mb-0 mt-3">
                Integer condimentum ipsum id imperdiet finibus. Vivamus in placerat mi, at euismod dui. Aliquam vitae
                neque eget nisl gravida pellentesque non ut velit.
              </p>
            </div>
          </div>
        </div>
        <div class="text-center">
          <button class="butn">More Info</button>
        </div>
      </div>
    </div>
    <div class="banner py-5 text-center">
      <div class="container my-5">
        <span class="top-text text-uppercase d-block">35.000+ already joined</span>
        <h2 class="my-5 w-50 mx-auto">Stay up-to-date with what we're doing</h2>
        <form :class="`d-flex align-items-stretch justify-content-center gap-3 ${validation.$error ? 'active' : ''}`" @submit.prevent="submission">
          <div :class="`input-cont position-relative ${validation.$error ? 'active-error' : ''}`">
            <input type="text" class="rounded-1 p-2 px-3 pe-5 h-100" placeholder="Enter your email adress"
              v-model="inputText.email">
            <span class="error fst-italic text-start w-100 px-3 p-2 position-absolute text-light d-block">
              {{ errorText }}
            </span>
            <img class="icon-error position-absolute" src="/images/icon-error.svg" alt="">
          </div>
          <input type="submit" class="butn rounded-1 text-capitalize" value="Contact Us">
        </form>
      </div>
    </div>
    <FooterComp></FooterComp>
  </main>
</template>
<script setup>
import HeaderNav from './components/HeaderNav.vue';
import { ref } from 'vue';
import { useVuelidate } from '@vuelidate/core'
import { required, email } from '@vuelidate/validators'
import FooterComp from './components/FooterComp.vue';


const activeTab = ref('tab-1')

const questOne = ref(false)
const questTwo = ref(false)
const questThree = ref(false)
const questFour = ref(false)


const inputText = ref({
  email: ''
})

const rules = {
  email: { required, email }
}

const errorText = ref('')

const validation = useVuelidate(rules, inputText)

const submission = () => {
  validation.value.$validate()
  if (!validation.value.$error) {
    window.location.reload()
  } else {
    if (validation.value.$errors[0].$validator === 'required') {
      errorText.value = 'Input can\'t be empty'
    } else errorText.value = 'Whoops, make sure it\'s an email'
  }
}

</script>
<style lang="scss">
* {
  box-sizing: border-box;
}

:root {
  // ### Primary
  --Soft-Blue: hsl(231, 69%, 60%);
  --Soft-Red: hsl(0, 94%, 66%);

  // ### Neutral
  --Grayish-Blue: hsl(229, 8%, 60%);
  --Very-Dark-Blue: hsl(229, 31%, 21%);
}

body {
  font-size: 18px;
  font-family: 'Rubik', sans-serif;
  min-height: 100vh;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.butn {
  outline: none;
  border-width: 2px;
  border-style: solid;
  border-color: var(--Soft-Red);
  background-color: var(--Soft-Red);
  color: white;
  padding: 5px 30px;
  border-radius: 5px;
  text-transform: uppercase;
  transition: 0.2s;
  box-shadow: 0 3px 8px var(--Grayish-Blue);

  &:hover {
    background-color: white;
    color: var(--Soft-Red);
  }
}

.heading {
  h1 {
    color: var(--Very-Dark-Blue);
  }

  p {
    color: var(--Grayish-Blue);
  }
}

.list-move,
/* apply transition to moving elements */
.list-enter-active,
.list-leave-active {
  transition: all 0.5s ease;
}

.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateX(-30px);
}

/* ensure leaving items are taken out of layout flow so that moving
   animations can be calculated correctly. */
.list-leave-active {
  position: absolute;
}


main {
  overflow: hidden;

  .landing {
    .info {
      h1 {
        color: var(--Very-Dark-Blue);
      }

      p {
        color: var(--Grayish-Blue);
      }

      .buttons {
        button {
          padding: 10px 30px;
          text-transform: initial;
          font-size: 15px;
        }

        button:first-child {
          background-color: var(--Soft-Blue);
          border-color: var(--Soft-Blue);

          &:hover {
            background-color: white;
            color: var(--Soft-Blue);
          }
        }

        button:last-child {
          background-color: whitesmoke;
          border-color: whitesmoke;
          box-shadow: 0 5px 20px rgb(211, 211, 211);
          color: var(--Very-Dark-Blue);

          &:hover {
            border-color: var(--Very-Dark-Blue);
            background-color: white;
          }
        }
      }
    }

    .hero {
      &::before {
        content: '';
        position: absolute;
        width: 950px;
        right: -75%;
        bottom: 0;
        height: 300px;
        border-radius: 550px;
        background-color: var(--Soft-Blue);
        z-index: -1;
      }
    }
  }

  .features {

    .tabs-butns {
      border-bottom: 3px solid rgb(236, 236, 236);
      position: relative;

      .tab {
        color: var(--Grayish-Blue);
        cursor: pointer;
        transition: 0.2s;

        &.active {
          color: var(--Very-Dark-Blue);
        }

        &.active-one~.slider {
          left: 0px;
        }

        &.active-two~.slider {
          left: 279px !important;
        }

        &.active-three~.slider {
          left: 558px;
        }
      }

      .slider {
        height: 5px;
        width: 279px;
        background-color: var(--Soft-Red);
        position: absolute;
        bottom: -3px;
        transition: 0.2s;
      }
    }

    .tabs-info {
      .feature {
        min-width: 536px;
        height: 346px;

        &::before {
          content: '';
          position: absolute;
          bottom: -75px;
          left: -120%;
          height: 300px;
          width: 950px;
          border-radius: 550px;
          background-color: var(--Soft-Blue);
          z-index: -1;
        }
      }

      .tabbing {
        .details {
          h2 {
            color: var(--Very-Dark-Blue);
          }

          p {
            color: var(--Grayish-Blue);
          }

          button {
            padding: 10px 20px;
            background-color: var(--Soft-Blue);
            border-color: var(--Soft-Blue);
            color: white;
            font-size: 15px;
            text-transform: capitalize;

            &:hover {
              background-color: white;
              color: var(--Soft-Blue);
            }
          }
        }
      }
    }
  }

  .extensions {
    .cards {
      .box {
        &:nth-child(1) {
          transform: translateY(-30px);
        }

        &:nth-child(3) {
          transform: translateY(30px);
        }
      }

      .extension-card {
        box-shadow: 0 5px 20px rgb(228, 228, 228);

        .icon-cont {
          height: 130px;
        }

        h4 {
          color: var(--Very-Dark-Blue);
          font-size: 20px;
        }

        span {
          color: var(--Grayish-Blue);
          font-size: 15px;
        }

        .dots {
          width: 100%;
        }

        button {
          background-color: var(--Soft-Blue);
          border-color: var(--Soft-Blue);
          text-transform: initial;
          padding: 11px;
          font-size: 15px;

          &:hover {
            background-color: white;
            color: var(--Soft-Blue);
          }
        }
      }
    }
  }

  .faq {
    .questions {
      .quest {
        cursor: pointer;
        position: relative;

        &:not(:last-child) {
          border-bottom: 1px solid rgb(219, 219, 219);
        }

        &:first-child {
          border-top: 1px solid rgb(219, 219, 219);
        }

        &:last-child {
          border-bottom: 1px solid rgb(219, 219, 219);
        }

        &:hover {
          h4 {
            color: var(--Soft-Red);
          }
        }

        h4 {
          transition: 0.2s;
          color: var(--Very-Dark-Blue);
          font-size: 18px;
        }

        svg {
          transition: 0.2s;
        }

        .quest-cont {
          overflow: hidden;
          opacity: 0;
          transform: translateY(-20px);
          height: 0;
          transition: 0.2s;

          p {
            color: var(--Grayish-Blue);
            line-height: 1.8;
          }
        }

        &.active {
          svg {
            transform: rotate(180deg);

            path {
              stroke: var(--Soft-Red);
            }
          }

          .quest-cont {
            height: 100%;
            transform: translateY(0px);
            opacity: 1;
          }
        }

      }
    }

    button {
      background-color: var(--Soft-Blue);
      border-color: var(--Soft-Blue);
      text-transform: capitalize;
      padding: 10px 20px;
      font-size: 15px;

      &:hover {
        background-color: white;
        color: var(--Soft-Blue);
      }
    }
  }

  .banner {
    background-color: var(--Soft-Blue);
    color: white;

    .top-text {
      font-size: 15px;
      letter-spacing: 5px;
    }

    form {
      .input-cont {
        .error {
          background-color: var(--Soft-Red);
          bottom: 0px;
          transition: 0.2s;
          font-size: 12px;
          border-bottom-left-radius: 3px;
          border-bottom-right-radius: 3px;
        }

        .icon-error {
          opacity: 0;
          right: 15px;
          z-index: 555555555;
          top: 50%;
          transition: 0.2s;
          transform: translateY(-50%);
        }

        input[type="text"] {
          border-width: 2px;
          border-style: solid;
          border-color: transparent;
          position: relative;
          z-index: 555555;
          outline: none;
          width: 350px;

          &::placeholder {
            color: var(--Grayish-Blue);
          }
        }

        &.active-error {
          .error {
            bottom: -30px;
          }

          .icon-error {
            opacity: 1;
          }

          input[type="text"] {
            border-color: var(--Soft-Red);
          }
        }
      }

      input[type="submit"] {
        font-size: 15px;
        padding: 12px 25px !important;
      }
    }
  }

  @media (max-width: 991px) {
    .landing {
      .hero {
        img {
          width: 100%;
        }
      }

      .info {
        text-align: center;
      }

      .buttons {
        justify-content: center;

        button {
          padding-left: 20px !important;
          padding-right: 20px !important;
        }
      }
    }

    .features {
      .heading {
        width: 100% !important;
      }

      .tabs-butns {
        width: 90% !important;
        flex-direction: column;
        border-bottom: none;

        .slider {
          display: none;
        }

        .tab {
          width: 100% !important;
          position: relative;

          &:first-child {
            border-top: 1px solid rgb(236, 236, 236);
          }

          border-bottom: 1px solid rgb(236, 236, 236);

          &::before {
            content: '';
            position: absolute;
            height: 5px;
            bottom: 0;
            width: 0;
            background-color: var(--Soft-Red);
            left: 50%;
            transform: translateX(-50%);
            transition: 0.2s;
          }

          &.active::before {
            width: 50%;
          }
        }
      }
      .tabbing {
        flex-direction: column;
        .feature {
          width: 100% !important;
          height: 100% !important;
          min-width: 0;
          img {
            width: 100% !important;
          }
          &::before {
            left: -95%;
          }
        }
        .details {
          text-align: center;
          width: 100% !important;
          margin-top: 50px;
        }
      }
    }
    .extensions {
      .heading {
        width: 100% !important;
      }
      .cards {
        .row {
          gap: 50px;
        }
        .box {
          &:nth-child(1) , &:nth-child(3) {
            transform: translateY(0px);
          }
        }
      }
    }
    .faq {
      .heading {
        width: 100% !important;
      }
      .questions {
        width: 100% !important;
        h4 {
          font-size: 15px !important;
        }
        p {
          font-size: 13px;
        }
      }
    }
    .banner {
      .top-text {
        font-size: 13px !important;
      }
      h2 {
        width: 100% !important;
        margin-top: 25px !important;
      }
      form {
        flex-direction: column;
        input {
          width: 100% !important;
          padding: 12px 25px !important;
        }
        &.active {
          gap: 50px !important;
        }
      }
    }
  }

  @media (max-width: 767px) {
    .landing {
      .hero {
        &::before {
          width: 550px;
          height: 200px;
        }
      }
    }
    .features {
      .tabbing {
        .feature::before {
          width: 550px;
          height: 200px;
          bottom: -35px;
          left: -70%;
        }
      }
    }
  }
}
</style>
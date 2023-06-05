<template>
  <div>
    <Header :loggedIn="false" />
    <div class="body">
        <div class="container">
            <div class="hero min-h-[80vh] max-h-[90vh] py-20 grid grid-cols-2">
              <div class="content flex flex-col ">
                <div class="mb-28">
                  <div class="mb-10">
                    <h1 class="text-blue-900 font-sora text-10xl font-semibold mb-4">Start monetizing your creations effortlessly</h1>
                    <p class="text-blue-100 font-inter text-lg">Effortlessly monetize your creations and turn your passion into profit with our user-friendly platform. Start generating revenue and connecting with your audience today.</p>
                  </div>
                  <div>
                    <a href="/home" class="border-2 border-blue-50 hover:border-blue-900 rounded-md py-3 px-6 text-blue-800 hover:text-blue-900 font-inter flex items-center gap-3 w-fit">
                      <span>
                        <svg width="17" height="16" viewBox="0 0 17 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                          <path d="M16.3869 8.18278C16.3869 7.59804 16.3342 7.03852 16.2364 6.50049H8.66797V9.58298L13.0268 9.58392C12.85 10.6095 12.281 11.4839 11.4093 12.0667V14.0666H14.0039C15.5189 12.6739 16.3869 10.6152 16.3869 8.18278Z" fill="#4285F4"/>
                          <path d="M11.4101 12.0663C10.6879 12.5502 9.75782 12.8332 8.66977 12.8332C6.56795 12.8332 4.78492 11.4265 4.14638 9.53027H1.46997V11.5927C2.79595 14.2063 5.52127 15.9998 8.66977 15.9998C10.8459 15.9998 12.674 15.2889 14.0047 14.0653L11.4101 12.0663Z" fill="#34A853"/>
                          <path d="M3.89438 8.00067C3.89438 7.46824 3.98372 6.95355 4.14641 6.4697V4.40723H1.47C0.921735 5.48797 0.613281 6.70789 0.613281 8.00067C0.613281 9.29345 0.922675 10.5134 1.47 11.5941L4.14641 9.53164C3.98372 9.04778 3.89438 8.5331 3.89438 8.00067Z" fill="#FABB05"/>
                          <path d="M8.66977 3.16656C9.85751 3.16656 10.9211 3.57289 11.7609 4.36686L14.0602 2.08489C12.6637 0.793042 10.8431 0 8.66977 0C5.52221 0 2.79595 1.79345 1.46997 4.40703L4.14638 6.4695C4.78492 4.5733 6.56795 3.16656 8.66977 3.16656Z" fill="#E94235"/>
                        </svg>
                        </span>Sign in with Google</a>
                  </div>
                </div>
                <div class="terms font-inter text-blue-100 flex gap-1">
                  Read our <a class="text-[#117DB6] hover:underline font-medium flex items-center gap-2" href="/terms">terms and conditions 
                  <span>
                    <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M5 3H3C2.44772 3 2 3.44772 2 4V9C2 9.55228 2.44772 10 3 10H8C8.55228 10 9 9.55228 9 9V7M7 2H10M10 2V5M10 2L5 7" stroke="#117DB6" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
                    </svg>
                  </span></a>
                </div>
              </div>
              <div class="bg flex max-w-xl">
                <img src="../static/assets/images/hero.svg" alt="hero-bg">
              </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import "/static/css/chargegpt.css"
import Header from '~/components/Header/Header.vue';
export default {
  name: 'IndexPage',
  components: {
    'Header': Header,
  },
  head: {
      script: [
          { src: "/static/js/main.js" },
          { src: "https://cdn.tailwindcss.com" },
      ],
  },
}
</script>

<template>
    <div>    
        <Header :loggedIn= "true" />
        <div class="container">
            <div id="create" class="flex flex-col py-20 max-w-3xl mx-auto">
                <div class="title mb-10">
                    <h1 class="font-sora text-8xl font-semibold text-blue-900 mb-5">Unleash the Power of Your Business!</h1>
                    <p class="font-inter text-xl text-blue-800">Share the exciting story of your business, its offerings, and what makes it truly unique. We'll transform your input into a captivating website that showcases your brand's personality and engages your target audience. Let's create something extraordinary together!</p>
                </div>
                <div class="p-4 border-2 rounded-md border-blue-100 border-dashed flex flex-col justify-between mb-8">
                    <textarea id="prompt" name="prompt" rows="5" cols="50">
                    </textarea>
                </div>
                <a @click="loadTheSite()" class="w-fit text-center font-medium inline-block py-3 px-16 border-2 border-blue-900 bg-blue-900 text-grey-50 rounded">Generate</a>
            </div>
        </div>
        <div id="loader-parent" class="min-h-[90vh] min-w-[100vw] flex justify-center items-center">
            <div id="load" class="loader-container hidden">
                <div class="loader"></div>
                <span id="loading-text" class="loader-text font-inter text-base text-blue-800 ml-4">Picking a color palette...</span>
            </div>
        </div>
        <div id="webpage" class="hidden">
            <img src="../../static/assets/images/sample-webpage.png" alt="Webpage" >
        </div>
    </div>
</template>

<script>
import "/static/css/chargegpt.css"
import Header from '~/components/Header/Header.vue';
import eventBus from '~/static/js/main.js';
export default {
    components: {
        'Header': Header,
    },

    data: function() {
        return {
            recording: false,
        }
    },

    methods: {
        loadTheSite : function () {
            var frame1 = document.getElementById('create');
            frame1.classList.add('hidden')

            var frame2 = document.getElementById('load');
            frame2.classList.remove('hidden')
            frame2.classList.add('flex')
        }
    },

    mounted() {
        const loadingText = document.getElementById('loading-text');
        var frame2 = document.getElementById('load');
        var frame4 = document.getElementById('loader-parent');
        const loadingPhrases = ['Picking a color palette...', 'Choosing relevant template...', 'Building product lineup...', 'Adding product gallery...', 'Adding attractive banners...', 'Adding testimonials...'];

        let index = 0;

        setInterval(() => {
            loadingText.textContent = loadingPhrases[index];
            index = (index + 1) % loadingPhrases.length;
            }, 1500);
        setInterval(() => {
            frame4.classList.add('hidden')
            frame2.classList.remove('flex')
            frame2.classList.add('hidden')

            var frame3 = document.getElementById('webpage');
            frame3.classList.remove('hidden')
            frame3.classList.add('block')
            
        }, 8000);
        }

    }
</script>

<style>

/* .loader-container {
  display: flex;
  align-items: center;
} */

.loader {
  border: 4px solid #f3f3f3;
  border-top: 4px solid #3498db;
  border-radius: 50%;
  width: 30px;
  height: 30px;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

</style>
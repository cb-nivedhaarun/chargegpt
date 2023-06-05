<template>
    <div>    
        <Header :loggedIn= "true" />
        <div class="container">
            <div id="site" class="flex flex-col py-20 max-w-3xl mx-auto">
                <div class="title mb-10">
                    <h1 class="font-sora text-8xl font-semibold text-blue-900 mb-5">Ready to embark on a digital journey?</h1>
                    <p class="font-inter text-xl text-blue-800">Whether you have an existing website or are starting from scratch, we'll create a captivating online presence that showcases the essence of your business.</p>
                </div>
                <div class="grid grid-cols-2 gap-16">
                    <div class="p-8 border-2 rounded-md border-blue-100 border-dashed flex flex-col justify-between">
                        <div>
                            <h2 class="font-sora text-lg text-blue-900 font-semibold mb-4">I have a website</h2>
                            <p class="font-inter text-base text-blue-100 mb-8">Ready to take your website to the next level? Prepare for an extraordinary online presence!</p>
                        </div>
                        <a href="#" class="text-center font-medium inline-block py-3 px-4 border-2 border-[#66CCF8] bg-[#66CCF8] text-[#0F5274] rounded">Connect your website</a>
                    </div>
                    <div class="p-8 border-2 rounded-md border-blue-100 border-dashed flex flex-col justify-between">
                        <div>
                            <h2 class="font-sora text-lg text-blue-900 font-semibold mb-4">No website? No problem!</h2>
                            <p class="font-inter text-base text-blue-100 mb-8">In just 60 seconds, we'll craft a stunning website that reflects your brand and captivates your audience.</p>
                        </div>
                        <a href="/create-your-site" class="text-center font-medium inline-block py-3 px-4 border-2 border-blue-900 bg-blue-900 text-grey-50 rounded">Create in 60 seconds</a>
                    </div>
                </div>
            </div>
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
        showRespectiveFrame : function (content) {
            var frame1 = document.getElementById('home');
            frame1.classList.add('hidden')

            var frame2 = document.getElementById('onboard');
            frame2.classList.remove('hidden')
            frame2.classList.add('flex')
        },
    },

    mounted() {

    }
}
</script>

<style>
</style>
<template>
  <div>
    <Header :loggedIn= "true" />
    <div>
        <div class="container">
            <div id="details" class="flex flex-col py-20 max-w-3xl mx-auto">
                <div>
                    <div class="title mb-10">
                        <h1 class="font-sora text-8xl font-semibold text-blue-900 mb-5">Kudos on providing the necessary information</h1>
                        <p class="font-inter text-xl text-blue-800 mb-4">We have displayed the details about your business, product offerings, pricing etc. on the screen. Please take a moment to review and confirm the accuracy before proceeding.</p>
                    </div>
                </div>
                <div class="mb-20">
                    <div class="border-2 border-grey-50 p-8 rounded-lg mb-8">
                        <div class="mb-8">
                            <h2 class="font-sora text-lg text-blue-900 font-semibold">Business</h2>
                        </div>
                        <div class="grid grid-cols-2 gap-y-10 gap-x-8">
                            <div>
                                <p class="font-sora text-lg text-blue-800 font-medium mb-2">Name</p>
                                <div class="py-2 px-3 border-2 border-blue-50 rounded-lg">
                                    <p class="font-inter text-lg text-blue-900">{{customerData.business.name}}</p>
                                </div>
                            </div>
                            <div>
                                <p class="font-sora text-lg text-blue-800 font-medium mb-2">Type</p>
                                <div class="py-2 px-3 border-2 border-blue-50 rounded-lg">
                                    <p class="font-inter text-lg text-blue-900">{{customerData.business.type}}</p>
                                </div>
                            </div>
                            <div>
                                <p class="font-sora text-lg text-blue-800 font-medium mb-2">Location</p>
                                <div class="py-2 px-3 border-2 border-blue-50 rounded-lg">
                                    <p class="font-inter text-lg text-blue-900">{{customerData.business.location}}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="border-2 border-grey-50 p-8 rounded-lg">
                        <div class="mb-8">
                            <h2 class="font-sora text-lg text-blue-900 font-semibold">Offerings</h2>
                        </div>
                        <div class="px-8">
                            <div>
                                <div class="grid grid-cols-3 gap-y-10 gap-x-8 mb-6">
                                    <div>
                                        <p class="font-sora text-lg text-blue-800 font-medium mb-2">Products</p>
                                    </div>
                                    <div>
                                        <p class="font-sora text-lg text-blue-800 font-medium mb-2">Frequency</p>
                                    </div>
                                    <div>
                                        <p class="font-sora text-lg text-blue-800 font-medium mb-2">Price</p>
                                    </div>
                                </div>
                            </div>
                            <div>
                                <template v-for="(plan, index) in customerData.plans">
                                    <div class="grid grid-cols-3 gap-x-8 mb-5" :key="index">
                                        <div class="text-blue-800 font-inter border-2 border-grey-50 p-2 px-4 rounded-lg">{{plan.name}}</div>
                                        <div class="text-blue-800 font-inter border-2 border-grey-50 p-2 px-4 rounded-lg">{{plan.frequency}}</div>
                                        <div class="text-blue-800 font-inter flex justify-between gap-8 border-2 border-grey-50 p-2 px-4 rounded-lg">
                                            <div >{{plan.price}}</div>
                                            <div>{{plan.currency}}</div>
                                        </div>
                                    </div>
                                </template>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="grid grid-cols-2">
                    <div class="block">
                        <div class="text-blue-100 font-inter text-base mb-5">Not painting the right picture?</div>
                        <a href="/home" class="inline-block py-3 px-4 border-2 border-[#66CCF8] text-[#117DB6] rounded">Start over</a>
                    </div>
                    <div class="items-end flex flex-col">
                        <div class="text-blue-100 font-inter text-base mb-5">Accurately represents your business?</div>
                        <a href="/site" class="w-fit inline-block py-3 px-4 border-2 border-blue-900 bg-blue-900 text-grey-50 rounded">Continue</a>
                    </div>
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
            customerData: {
                "business": {
                    name: "CrustLove",
                    type: "Food Startup",
                    location: "Newyork"
                },
                "plans": [
                    {
                    "name": "Bread",
                    frequency: "Daily",
                    "id": "bread_daily_USD",
                    "price": 5.99,
                    "currency": "USD"
                    },
                    {
                    "name": "Bread",
                    frequency: "Weekly",
                    "id": "bread_weekly_USD",
                    "price": 19.99,
                    "currency": "USD"
                    },
                    {
                    "name": "Bread Subscription",
                    frequency: "Monthly",
                    "id": "bread_monthly_USD",
                    "price": 85.99,
                    "currency": "USD"
                    },
                    {
                    "name": "Pastry Subscription",
                    frequency: "Daily",
                    "id": "pastry_daily_USD",
                    "price": 7.99,
                    "currency": "USD"
                    },
                    {
                    "name": "Pastry Subscription",
                    frequency: "Weekly",
                    "id": "pastry_weekly_USD",
                    "price": 12.99,
                    "currency": "USD"
                    },
                    {
                    "name": "Pastry Subscription",
                    frequency: "Monthly",
                    "id": "pastry_monthly_USD",
                    "price": 34.99,
                    "currency": "USD"
                    },
                    {
                    "name": "Coffee Subscription",
                    frequency: "Daily",
                    "id": "coffee_daily_USD",
                    "price": 7.99,
                    "currency": "USD"
                    },
                    {
                    "name": "Coffee Subscription",
                    frequency: "Weekly",
                    "id": "coffee_weekly_USD",
                    "price": 14.99,
                    "currency": "USD"
                    },
                    {
                    "name": "Coffee Subscription",
                    frequency: "Monthly",
                    "id": "coffee_monthly_USD",
                    "price": 26.99,
                    "currency": "USD"
                    },
                    {
                    "name": "Bread Subscription",
                    frequency: "Daily",
                    "id": "bread_daily_EUR",
                    "price": 5.99,
                    "currency": "EUR"
                    },
                    {
                    "name": "Bread Subscription",
                    frequency: "Weekly",
                    "id": "bread_weekly_EUR",
                    "price": 19.99,
                    "currency": "EUR"
                    },
                    {
                    "name": "Bread Subscription",
                    frequency: "Monthly",
                    "id": "bread_monthly_EUR",
                    "price": 85.99,
                    "currency": "EUR"
                    },
                    {
                    "name": "Pastry Subscription",
                    frequency: "Daily",
                    "id": "pastry_daily_EUR",
                    "price": 7.99,
                    "currency": "EUR"
                    },
                    {
                    "name": "Pastry Subscription",
                    frequency: "Weekly",
                    "id": "pastry_weekly_EUR",
                    "price": 12.99,
                    "currency": "EUR"
                    },
                    {
                    "name": "Pastry Subscription",
                    frequency: "Monthly",
                    "id": "pastry_monthly_EUR",
                    "price": 34.99,
                    "currency": "EUR"
                    },
                    {
                    "name": "Coffee Subscription",
                    frequency: "Daily",
                    "id": "coffee_daily_EUR",
                    "price": 7.99,
                    "currency": "EUR"
                    },
                    {
                    "name": "Coffee Subscription",
                    frequency: "Weekly",
                    "id": "coffee_weekly_EUR",
                    "price": 14.99,
                    "currency": "EUR"
                    },
                    {
                    "name": "Coffee Subscription",
                    frequency: "Monthly",
                    "id": "coffee_monthly_EUR",
                    "price": 26.99,
                    "currency": "EUR"
                    }
                ]
}
,
        }
    },
    created() {
        eventBus.$on('audio', this.updateMessage);
    },
    methods: {
        updateMessage(data) {
        this.audio = data;
        },
    },
    
    mounted() {
        console.log(this.audio)
    }
}
</script>

<style>

</style>
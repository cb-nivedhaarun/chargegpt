<template>
    <div>    
        <Header />
        <div class="container">
            <div id="home" class="flex flex-col py-20 max-w-3xl mx-auto">
                <div class="title mb-10">
                    <h1 class="font-sora text-8xl font-semibold text-blue-900 mb-5">Welcome, John!</h1>
                    <p class="font-inter text-xl text-blue-800">To kickstart your journey, let us know about your business. Just use your voice and we'll handle the rest.</p>
                </div>
                <div class="note mb-20">
                    <div class="flex items-center gap-3 text-blue-800 bg-[#E7FAFF] w-fit py-3 px-6 rounded">
                    <span>
                        <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" clip-rule="evenodd" d="M19.6 9.9999C19.6 15.3018 15.3019 19.5999 9.99999 19.5999C4.69806 19.5999 0.399994 15.3018 0.399994 9.9999C0.399994 4.69797 4.69806 0.399902 9.99999 0.399902C15.3019 0.399902 19.6 4.69797 19.6 9.9999ZM11.2 5.1999C11.2 5.86264 10.6627 6.3999 9.99999 6.3999C9.33725 6.3999 8.79999 5.86264 8.79999 5.1999C8.79999 4.53716 9.33725 3.9999 9.99999 3.9999C10.6627 3.9999 11.2 4.53716 11.2 5.1999ZM8.79999 8.7999C8.13725 8.7999 7.59999 9.33716 7.59999 9.9999C7.59999 10.6626 8.13725 11.1999 8.79999 11.1999V14.7999C8.79999 15.4626 9.33725 15.9999 9.99999 15.9999H11.2C11.8627 15.9999 12.4 15.4626 12.4 14.7999C12.4 14.1372 11.8627 13.5999 11.2 13.5999V9.9999C11.2 9.33716 10.6627 8.7999 9.99999 8.7999H8.79999Z" fill="#2E9FD9"/>
                        </svg>
                    </span>
                    <p class="font-inter text-sm">Feel confident knowing that your onboarding progress will be saved as we go.</p>
                    </div>
                </div>
                <a @click="showRespectiveFrame('onboard')" class="cursor-pointer cta py-3 px-4 text-grey-50 bg-blue-900 rounded w-fit hover:text-blue-900 hover:bg-lime-500">
                    Let's dive in
                </a>
            </div>
            <div id="onboard" class="flex-col py-20 max-w-3xl mx-auto hidden"> 
                <div id="record-content">
                    <div class="title mb-10">
                        <h1 class="font-sora text-8xl font-semibold text-blue-900 mb-5">Get ready for an effortless onboarding</h1>
                        <p class="font-inter text-xl text-blue-800 mb-4">Hit record and feel free to speak casually about your business, covering important details such as your business name, type, location, products, pricing, and subscriptions. Take your time to do so. Once you're done, we'll display the information for your confirmation.</p>
                        <p class="font-inter text-xl text-blue-100">We have given a sample below for you to get started</p>
                    </div>
                    <div class="sample mb-8">
                        <div class="p-4 border-2 rounded-md border-blue-100 border-dashed">
                            <p class="font-inter text-base text-blue-100">Hey, it's Lisa from FitConnect. We're a fitness startup based in San Francisco. At FitConnect, we offer a subscription-based fitness app that provides Personalised Workout Plans. Our app features different levels of workout plans: Starter, priced at around $9.99/month, Pro at around $19.99/month, and Elite at approximately $29.99/month. To enhance the fitness experience, we also offer add-ons to the workout plans, such as Nutrition Coaching and Live Virtual Classes, which come at an additional cost of $5/month. Additionally, we provide Progress Tracking and Analytics as an add-on for $3/month.</p>
                        </div>
                    </div>
                </div>
                <div id="recording-image" class="flex-col items-center hidden mb-24">
                    <svg width="474" height="240" viewBox="0 0 474 240" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <g opacity="0.7">
                        <path d="M472.966 118.168C467.941 135.813 461.605 127.439 460.512 124.349L457.672 116.473C455.05 109.296 451.773 109.296 450.243 116.573L447.84 129.034C445.218 142.392 441.941 142.392 440.411 128.934L438.008 107.302C436.479 93.9438 433.201 93.8441 430.58 107.202L427.739 122.156C426.647 128.037 423.369 128.137 420.311 122.355L418.781 119.464C417.033 116.075 413.756 116.075 411.571 119.364L409.168 122.953C407.42 125.445 404.361 125.445 402.176 123.053L398.899 119.364C397.588 117.769 394.529 117.67 392.344 119.065L389.504 120.86C387.756 121.956 385.134 121.956 383.386 120.86L382.075 120.062C379.017 118.168 375.958 118.467 375.302 120.86L372.681 129.433C370.496 137.009 367.218 137.009 365.252 129.433L361.538 114.579C360.008 108.399 356.731 108.299 354.109 114.48L353.672 115.676C351.05 121.856 347.773 121.757 346.244 115.576L343.84 105.508C341.218 94.9406 337.941 94.9406 336.412 105.607L332.042 135.314C330.513 145.283 327.235 145.283 324.614 135.414L320.899 121.059C320.244 118.666 317.185 118.268 314.126 120.261L313.252 120.76C311.286 121.956 308.664 121.856 306.916 120.66L306.042 120.062C303.857 118.268 300.798 118.367 299.269 120.361L296.866 123.551C294.244 127.14 290.967 126.941 289.656 123.252L285.504 111.888C283.757 107.202 280.479 107.202 278.076 111.788L274.799 118.168C273.488 120.76 270.429 120.959 267.807 118.567L266.059 116.872C264.311 115.078 261.252 115.078 259.286 116.872L255.572 120.361C254.042 121.757 251.202 121.956 249.236 120.66L247.706 119.663C245.084 118.068 242.244 118.268 241.152 120.162L239.404 123.252C237.219 126.941 233.942 126.941 232.194 123.152L228.698 115.676C227.169 112.386 223.891 112.286 221.488 115.476L218.429 119.763C217.118 121.458 214.278 121.657 211.874 120.162L211.001 119.564C208.379 117.969 205.538 118.168 204.446 120.062L200.95 125.844C198.547 129.732 195.269 129.732 193.74 125.744L191.118 119.564C188.933 114.081 185.438 114.081 183.69 119.663L181.068 127.539C178.883 134.517 175.606 134.417 173.639 127.539L171.673 120.062C169.27 110.99 165.992 110.99 164.244 120.162L163.152 125.545C160.967 137.009 157.69 137.009 155.723 125.545L153.539 112.885C151.354 100.423 148.076 100.423 146.11 112.885L143.707 128.037C141.522 141.993 138.245 141.993 136.278 128.037L133.438 108.399C131.471 94.5419 128.194 94.5419 126.009 108.399L123.606 123.252C122.732 128.735 119.455 128.835 116.177 123.551L113.556 119.065C111.808 116.075 108.53 116.075 106.345 118.965L103.942 122.255C101.976 124.847 98.9169 124.847 96.9505 122.255L95.2026 119.863C93.8917 118.168 90.8329 117.969 88.648 119.464L86.0262 121.059C84.2783 122.156 81.6565 122.156 79.9086 121.059L78.3792 120.062C75.5389 118.268 72.48 118.567 71.6061 120.76L68.1103 130.131C65.4885 137.308 62.2112 137.308 60.6818 130.031L56.749 109.395C55.0011 100.523 51.7238 100.523 49.3205 109.296L46.2617 121.059C44.9507 125.944 41.6734 126.043 38.8331 121.258L36.6482 117.57C35.1188 114.978 32.06 114.878 29.6567 117.271L27.2533 119.863C25.5054 121.557 22.6651 121.657 20.4802 120.062C18.2954 118.268 15.2366 118.367 13.7072 120.361L10.6483 124.448C8.46348 127.539 4.96769 128.536 1.25342 119.962" stroke="#CDD2DB" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
                        <path d="M1.03467 119.564L5.84137 128.237C8.6817 133.321 11.7405 133.022 13.0514 127.539L15.8918 113.782C18.5136 101.121 21.7909 101.221 23.3203 113.981L25.7237 136.012C28.3455 159.539 31.6228 159.439 33.1522 135.913L35.5555 97.732C37.085 74.106 40.3623 74.106 42.9841 97.6324L45.8244 124.05C46.9168 134.417 50.1941 134.617 53.253 124.448L54.7824 119.364C56.5303 113.483 59.8076 113.383 61.9924 119.165L64.3958 125.545C66.1437 129.931 69.2025 130.031 71.3873 125.744L74.6646 119.165C75.9756 116.374 79.0344 116.075 81.2192 118.567L84.0596 121.757C85.8075 123.651 88.4293 123.651 90.1772 121.757L91.4881 120.361C94.5469 116.972 97.6057 117.57 98.2612 121.657L100.883 136.71C103.068 149.969 106.345 149.969 108.312 136.61L112.026 110.392C113.555 99.5264 116.833 99.4267 119.454 110.193L119.891 112.187C122.513 123.053 125.79 122.953 127.32 111.987L129.723 94.243C132.345 75.6013 135.622 75.6013 137.152 94.3427L141.522 146.779C143.051 164.324 146.328 164.423 148.95 146.978L152.664 121.757C153.32 117.57 156.379 116.872 159.437 120.361L160.311 121.258C162.278 123.352 164.9 123.252 166.647 120.959L167.521 119.863C169.706 116.673 172.765 116.872 174.295 120.361L176.698 126.043C179.32 132.324 182.597 132.124 183.908 125.545L188.059 105.508C189.807 97.2336 193.084 97.2336 195.488 105.308L198.11 116.673C199.42 121.358 202.479 121.558 205.101 117.271L206.849 114.28C208.597 111.19 211.656 111.19 213.622 114.28L217.336 120.461C218.866 122.953 221.706 123.153 223.672 120.959L225.202 119.265C227.824 116.374 230.664 116.872 231.756 120.262L233.504 125.645C235.689 132.224 238.967 132.124 240.714 125.545L244.21 112.386C245.74 106.604 249.017 106.405 251.42 112.087L254.479 119.663C255.79 122.754 258.63 123.053 261.034 120.461L261.908 119.364C264.529 116.573 267.37 116.972 268.462 120.361L271.958 130.629C274.361 137.508 277.639 137.408 279.168 130.43L281.79 119.464C283.975 109.794 287.471 109.894 289.218 119.564L291.84 133.42C294.025 145.582 297.302 145.582 299.269 133.321L301.235 120.062C303.639 104.012 306.916 104.112 308.664 120.162L309.756 129.732C311.941 149.969 315.218 149.969 317.185 129.732L319.37 107.501C321.554 85.4704 324.832 85.5701 326.798 107.501L329.201 134.218C331.386 158.841 334.664 158.841 336.63 134.218L339.47 99.6261C341.437 75.2025 344.714 75.1028 346.899 99.6261L349.302 125.744C350.176 135.414 353.454 135.614 356.731 126.343L359.353 118.367C361.101 113.184 364.378 113.084 366.563 118.168L369.185 123.651C371.151 128.237 374.21 128.237 376.176 123.651L377.924 119.464C379.235 116.473 382.294 116.075 384.479 118.667L387.1 121.558C388.848 123.452 391.47 123.452 393.218 121.558L394.747 119.863C397.588 116.573 400.647 117.171 401.521 121.159L405.016 137.707C407.638 150.367 410.915 150.268 412.445 137.508L416.378 101.121C418.126 85.4704 421.403 85.4704 423.806 101.022L426.865 121.657C428.176 130.33 431.453 130.529 434.294 122.056L436.478 115.477C438.008 110.891 441.067 110.692 443.47 114.978L445.873 119.464C447.621 122.455 450.462 122.554 452.646 119.763C454.831 116.573 457.89 116.772 459.42 120.262L462.478 127.439C464.663 132.922 467.94 132.822 469.688 127.14L472.529 117.769" stroke="#117DB6" stroke-width="2" stroke-miterlimit="10" stroke-linecap="round" stroke-linejoin="round"/>
                        </g>
                    </svg>
                    <p class="font-inter text-xl text-blue-800 mb-4 text-center">Take your time to share what your business does without worrying about structure. Hit stop when you're satisfied.</p>
                </div>
                <div>
                    <div class="audio-recording-container">
                        <div @click="recordAudio()" class="start-recording-button fa fa-microphone" aria-hidden="true">
                            <svg width="120" height="120" viewBox="0 0 120 120" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <g filter="url(#filter0_d_4815_987)">
                                <rect x="20" y="20" width="80" height="80" rx="40" fill="#012A38"/>
                                <path d="M55 50C55 47.2386 57.2386 45 60 45C62.7614 45 65 47.2386 65 50V61C65 63.7614 62.7614 66 60 66C57.2386 66 55 63.7614 55 61V50Z" fill="#E7FAFF"/>
                                <path d="M52 58C52.5523 58 53 58.4477 53 59V61C53 64.866 56.134 68 60 68C63.866 68 67 64.866 67 61V59C67 58.4477 67.4477 58 68 58C68.5523 58 69 58.4477 69 59V61C69 65.6326 65.5 69.4476 61 69.9451V73H65C65.5523 73 66 73.4477 66 74C66 74.5523 65.5523 75 65 75H55C54.4477 75 54 74.5523 54 74C54 73.4477 54.4477 73 55 73H59V69.9451C54.5 69.4476 51 65.6326 51 61V59C51 58.4477 51.4477 58 52 58Z" fill="#E7FAFF"/>
                                </g>
                                <defs>
                                <filter id="filter0_d_4815_987" x="0" y="0" width="120" height="120" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                                <feFlood flood-opacity="0" result="BackgroundImageFix"/>
                                <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
                                <feOffset/>
                                <feGaussianBlur stdDeviation="10"/>
                                <feComposite in2="hardAlpha" operator="out"/>
                                <feColorMatrix type="matrix" values="0 0 0 0 0.803922 0 0 0 0 0.823529 0 0 0 0 0.858824 0 0 0 1 0"/>
                                <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_4815_987"/>
                                <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_4815_987" result="shape"/>
                                </filter>
                                </defs>
                            </svg>
                        </div>
                        <a href="/details" id="submit" class="hidden" aria-hidden="true">
                            <svg width="72" height="72" viewBox="0 0 72 72" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <rect width="72" height="72" rx="36" fill="#117DB6"/>
                                <path fill-rule="evenodd" clip-rule="evenodd" d="M36.9697 27.9697C37.2626 27.6768 37.7374 27.6768 38.0303 27.9697L45.5303 35.4697C45.671 35.6103 45.75 35.8011 45.75 36C45.75 36.1989 45.671 36.3897 45.5303 36.5303L38.0303 44.0303C37.7374 44.3232 37.2626 44.3232 36.9697 44.0303C36.6768 43.7374 36.6768 43.2626 36.9697 42.9697L43.1893 36.75H27C26.5858 36.75 26.25 36.4142 26.25 36C26.25 35.5858 26.5858 35.25 27 35.25H43.1893L36.9697 29.0303C36.6768 28.7374 36.6768 28.2626 36.9697 27.9697Z" fill="white"/>
                            </svg>
                        </a>
                        <div class="recording-contorl-buttons-container hide">
                            <div class="cancel-recording-button fa fa-times-circle-o" aria-hidden="true">
                                <svg width="107" height="107" viewBox="0 0 107 107" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <g filter="url(#filter0_d_4843_223)">
                                    <rect x="20" y="20" width="67" height="67" rx="33.5" fill="#117DB6"/>
                                    <path fill-rule="evenodd" clip-rule="evenodd" d="M46.9697 46.9697C47.2626 46.6768 47.7374 46.6768 48.0303 46.9697L53.5 52.4393L58.9697 46.9697C59.2626 46.6768 59.7374 46.6768 60.0303 46.9697C60.3232 47.2626 60.3232 47.7374 60.0303 48.0303L54.5607 53.5L60.0303 58.9697C60.3232 59.2626 60.3232 59.7374 60.0303 60.0303C59.7374 60.3232 59.2626 60.3232 58.9697 60.0303L53.5 54.5607L48.0303 60.0303C47.7374 60.3232 47.2626 60.3232 46.9697 60.0303C46.6768 59.7374 46.6768 59.2626 46.9697 58.9697L52.4393 53.5L46.9697 48.0303C46.6768 47.7374 46.6768 47.2626 46.9697 46.9697Z" fill="#EFEFEF"/>
                                    </g>
                                    <defs>
                                    <filter id="filter0_d_4843_223" x="0" y="0" width="107" height="107" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                                    <feFlood flood-opacity="0" result="BackgroundImageFix"/>
                                    <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
                                    <feOffset/>
                                    <feGaussianBlur stdDeviation="10"/>
                                    <feComposite in2="hardAlpha" operator="out"/>
                                    <feColorMatrix type="matrix" values="0 0 0 0 0.803922 0 0 0 0 0.823529 0 0 0 0 0.858824 0 0 0 1 0"/>
                                    <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_4843_223"/>
                                    <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_4843_223" result="shape"/>
                                    </filter>
                                    </defs>
                                </svg>
                            </div>
                            <div class="recording-elapsed-time">
                                <div class="red-recording-dot fa fa-circle" aria-hidden="true">
                                    <svg width="108" height="108" viewBox="0 0 108 108" fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <g filter="url(#filter0_d_4843_219)">
                                        <rect x="20" y="20" width="67.5" height="67.5" rx="33.75" fill="#E49999"/>
                                        <path fill-rule="evenodd" clip-rule="evenodd" d="M44 53.75C44 48.3652 48.3652 44 53.75 44C59.1348 44 63.5 48.3652 63.5 53.75C63.5 59.1348 59.1348 63.5 53.75 63.5C48.3652 63.5 44 59.1348 44 53.75Z" fill="#EFEFEF"/>
                                        </g>
                                        <defs>
                                        <filter id="filter0_d_4843_219" x="0" y="0" width="107.5" height="107.5" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                                        <feFlood flood-opacity="0" result="BackgroundImageFix"/>
                                        <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
                                        <feOffset/>
                                        <feGaussianBlur stdDeviation="10"/>
                                        <feComposite in2="hardAlpha" operator="out"/>
                                        <feColorMatrix type="matrix" values="0 0 0 0 0.803922 0 0 0 0 0.823529 0 0 0 0 0.858824 0 0 0 1 0"/>
                                        <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_4843_219"/>
                                        <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_4843_219" result="shape"/>
                                        </filter>
                                        </defs>
                                    </svg>
                                </div>
                                <p class="elapsed-time"></p>
                            </div>
                            <div class="stop-recording-button fa fa-stop-circle-o" aria-hidden="true">
                                <svg width="120" height="120" viewBox="0 0 120 120" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <g filter="url(#filter0_d_4815_1114)">
                                    <rect x="20" y="20" width="80" height="80" rx="40" fill="#117DB6"/>
                                    <path fill-rule="evenodd" clip-rule="evenodd" d="M50 54C50 51.7909 51.7909 50 54 50H66C68.2091 50 70 51.7909 70 54V66C70 68.2091 68.2091 70 66 70H54C51.7909 70 50 68.2091 50 66V54Z" fill="white"/>
                                    </g>
                                    <defs>
                                    <filter id="filter0_d_4815_1114" x="0" y="0" width="120" height="120" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                                    <feFlood flood-opacity="0" result="BackgroundImageFix"/>
                                    <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
                                    <feOffset/>
                                    <feGaussianBlur stdDeviation="10"/>
                                    <feComposite in2="hardAlpha" operator="out"/>
                                    <feColorMatrix type="matrix" values="0 0 0 0 0.803922 0 0 0 0 0.823529 0 0 0 0 0.858824 0 0 0 1 0"/>
                                    <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_4815_1114"/>
                                    <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_4815_1114" result="shape"/>
                                    </filter>
                                    </defs>
                                </svg>
                            </div>
                        </div>
                        <div class="text-indication-of-audio-playing-container">
                            <p class="text-indication-of-audio-playing hide">Audio is playing<span>.</span><span>.</span><span>.</span></p>
                        </div>
                    </div>
                    <div class="overlay hide">
                        <div class="browser-not-supporting-audio-recording-box">
                            <p>To record audio, use browsers like Chrome and Firefox that support audio recording.</p>
                            <button type="button" class="close-browser-not-supported-box">Ok.</button>
                        </div>
                    </div>

                    <audio controls class="audio-element hide">
                    </audio>
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
        recordAudio : function (){

            var self = this;

            //View
            var microphoneButton = document.getElementsByClassName("start-recording-button")[0];
            var recordingControlButtonsContainer = document.getElementsByClassName("recording-contorl-buttons-container")[0];
            var stopRecordingButton = document.getElementsByClassName("stop-recording-button")[0];
            var cancelRecordingButton = document.getElementsByClassName("cancel-recording-button")[0];
            var elapsedTimeTag = document.getElementsByClassName("elapsed-time")[0];
            var closeBrowserNotSupportedBoxButton = document.getElementsByClassName("close-browser-not-supported-box")[0];
            var overlay = document.getElementsByClassName("overlay")[0];
            var audioElement = document.getElementsByClassName("audio-element")[0];
            var audioElementSource = document.getElementsByClassName("audio-element")[0]
                .getElementsByTagName("source")[0];
            var textIndicatorOfAudiPlaying = document.getElementsByClassName("text-indication-of-audio-playing")[0];
            var proceedWithAudio = document.getElementById("submit");
            var sampleRecordContent = document.getElementById("record-content");
            var recordImage = document.getElementById("recording-image");

            //Listeners

            //Listen to stop recording button
            stopRecordingButton.onclick = stopAudioRecording;

            //Listen to cancel recording button
            cancelRecordingButton.onclick = cancelAudioRecording;

            //Listen to when the ok button is clicked in the browser not supporting audio recording box
            closeBrowserNotSupportedBoxButton.onclick = hideBrowserNotSupportedOverlay;

            //Listen to when the audio being played ends
            audioElement.onended = hideTextIndicatorOfAudioPlaying;

            /** Displays recording control buttons */
            function handleDisplayingRecordingControlButtons() {
                //Hide the microphone button that starts audio recording
                microphoneButton.style.display = "none";

                //Display the recording control buttons
                recordingControlButtonsContainer.classList.remove("hide");

                //Handle the displaying of the elapsed recording time
                handleElapsedRecordingTime();
            }

            /** Hide the displayed recording control buttons */
            function handleHidingRecordingControlButtons() {
                //Display the microphone button that starts audio recording
                microphoneButton.style.display = "block";

                //Hide the recording control buttons
                recordingControlButtonsContainer.classList.add("hide");

                //stop interval that handles both time elapsed and the red dot
                clearInterval(elapsedTimeTimer);
            }

            /** Displays browser not supported info box for the user*/
            function displayBrowserNotSupportedOverlay() {
                overlay.classList.remove("hide");
            }

            /** Displays browser not supported info box for the user*/
            function hideBrowserNotSupportedOverlay() {
                overlay.classList.add("hide");
            }

            /** Creates a source element for the the audio element in the HTML document*/
            function createSourceForAudioElement() {
                let sourceElement = document.createElement("source");
                audioElement.appendChild(sourceElement);

                audioElementSource = sourceElement;
            }

            /** Display the text indicator of the audio being playing in the background */
            function displayTextIndicatorOfAudioPlaying() {
                textIndicatorOfAudiPlaying.classList.remove("hide");
            }

            /** Hide the text indicator of the audio being playing in the background */
            function hideTextIndicatorOfAudioPlaying() {
                textIndicatorOfAudiPlaying.classList.add("hide");
                microphoneButton.style.display = "none";
                proceedWithAudio.classList.remove("hidden")
                proceedWithAudio.classList.add("block")

            }

            //Controller

            /** Stores the actual start time when an audio recording begins to take place to ensure elapsed time start time is accurate*/
            var audioRecordStartTime;

            /** Stores the maximum recording time in hours to stop recording once maximum recording hour has been reached */
            var maximumRecordingTimeInHours = 1;

            /** Stores the reference of the setInterval function that controls the timer in audio recording*/
            var elapsedTimeTimer;

            /** Starts the audio recording*/
            function startAudioRecording() {

                console.log("Recording Audio...");
                self.recording = true;

                sampleRecordContent.style.display = "none";
                recordImage.style.display = "flex"

                //If a previous audio recording is playing, pause it
                let recorderAudioIsPlaying = !audioElement.paused; // the paused property tells whether the media element is paused or not
                console.log("paused?", !recorderAudioIsPlaying);
                if (recorderAudioIsPlaying) {
                    audioElement.pause();
                    //also hide the audio playing indicator displayed on the screen
                    hideTextIndicatorOfAudioPlaying();
                }

                //start recording using the audio recording API
                audioRecorder.start()
                    .then(() => { //on success

                        //store the recording start time to display the elapsed time according to it
                        audioRecordStartTime = new Date();

                        //display control buttons to offer the functionality of stop and cancel
                        handleDisplayingRecordingControlButtons();
                    })
                    .catch(error => { //on error
                        //No Browser Support Error
                        if (error.message.includes("mediaDevices API or getUserMedia method is not supported in this browser.")) {
                            console.log("To record audio, use browsers like Chrome and Firefox.");
                            displayBrowserNotSupportedOverlay();
                        }

                        //Error handling structure
                        switch (error.name) {
                            case 'AbortError': //error from navigator.mediaDevices.getUserMedia
                                console.log("An AbortError has occured.");
                                break;
                            case 'NotAllowedError': //error from navigator.mediaDevices.getUserMedia
                                console.log("A NotAllowedError has occured. User might have denied permission.");
                                break;
                            case 'NotFoundError': //error from navigator.mediaDevices.getUserMedia
                                console.log("A NotFoundError has occured.");
                                break;
                            case 'NotReadableError': //error from navigator.mediaDevices.getUserMedia
                                console.log("A NotReadableError has occured.");
                                break;
                            case 'SecurityError': //error from navigator.mediaDevices.getUserMedia or from the MediaRecorder.start
                                console.log("A SecurityError has occured.");
                                break;
                            case 'TypeError': //error from navigator.mediaDevices.getUserMedia
                                console.log("A TypeError has occured.");
                                break;
                            case 'InvalidStateError': //error from the MediaRecorder.start
                                console.log("An InvalidStateError has occured.");
                                break;
                            case 'UnknownError': //error from the MediaRecorder.start
                                console.log("An UnknownError has occured.");
                                break;
                            default:
                                console.log("An error occured with the error name " + error.name);
                        };
                    });
            }
            /** Stop the currently started audio recording & sends it
            */
            function stopAudioRecording() {

                console.log("Stopping Audio Recording...");

                //stop the recording using the audio recording API
                audioRecorder.stop()
                    .then(audioAsblob => {
                        //Play recorder audio
                        playAudio(audioAsblob);

                        //hide recording control button & return record icon
                        handleHidingRecordingControlButtons();
                    })
                    .catch(error => {
                        //Error handling structure
                        switch (error.name) {
                            case 'InvalidStateError': //error from the MediaRecorder.stop
                                console.log("An InvalidStateError has occured.");
                                break;
                            default:
                                console.log("An error occured with the error name " + error.name);
                        };
                    });
            }

            /** Cancel the currently started audio recording */
            function cancelAudioRecording() {
                console.log("Canceling audio...");

                //cancel the recording using the audio recording API
                audioRecorder.cancel();

                //hide recording control button & return record icon
                handleHidingRecordingControlButtons();
            }

            /** Plays recorded audio using the audio element in the HTML document
            * @param {Blob} recorderAudioAsBlob - recorded audio as a Blob Object 
            */
            function playAudio(recorderAudioAsBlob) {

                //read content of files (Blobs) asynchronously
                let reader = new FileReader();

                //once content has been read
                reader.onload = (e) => {
                    //store the base64 URL that represents the URL of the recording audio
                    let base64URL = e.target.result;


                    function setGlobalData(data) {
                        console.log(data)
                        eventBus.$emit('audio', data);
                    }

                    function saveFileToVariable(data64) {
                        return fetch(data64)
                            .then(response => response.blob())
                            .then(blob => {
                            self.audioFile = blob   
                            setGlobalData(self.audioFile)
                            return blob;
                            })
                            .catch(error => {
                            console.error('Error fetching the audio file:', error);
                        });
                    }

                    //If this is the first audio playing, create a source element
                    //as pre populating the HTML with a source of empty src causes error
                    if (!audioElementSource) //if its not defined create it (happens first time only)
                        createSourceForAudioElement();

                    //set the audio element's source using the base64 URL
                    audioElementSource.src = base64URL;

                    //set the type of the audio element based on the recorded audio's Blob type
                    let BlobType = recorderAudioAsBlob.type.includes(";") ?
                        recorderAudioAsBlob.type.substr(0, recorderAudioAsBlob.type.indexOf(';')) : recorderAudioAsBlob.type;
                    audioElementSource.type = BlobType

                    //call the load method as it is used to update the audio element after changing the source or other settings
                    audioElement.load();

                    saveFileToVariable(base64URL);

                    //play the audio after successfully setting new src and type that corresponds to the recorded audio
                    console.log("Playing audio...");
                    audioElement.play();

                    var audioData = base64URL
                    console.log(audioData)
                    //Display text indicator of having the audio play in the background
                    displayTextIndicatorOfAudioPlaying();
                };

                //read content and convert it to a URL (base64)
                reader.readAsDataURL(recorderAudioAsBlob);
            }

            /** Computes the elapsed recording time since the moment the function is called in the format h:m:s*/
            function handleElapsedRecordingTime() {
                //display inital time when recording begins
                displayElapsedTimeDuringAudioRecording("00:00");

                //create an interval that compute & displays elapsed time, as well as, animate red dot - every second
                elapsedTimeTimer = setInterval(() => {
                    //compute the elapsed time every second
                    let elapsedTime = computeElapsedTime(audioRecordStartTime); //pass the actual record start time
                    //display the elapsed time
                    displayElapsedTimeDuringAudioRecording(elapsedTime);
                }, 1000); //every second
            }

            /** Display elapsed time during audio recording
            * @param {String} elapsedTime - elapsed time in the format mm:ss or hh:mm:ss 
            */
            function displayElapsedTimeDuringAudioRecording(elapsedTime) {
                //1. display the passed elapsed time as the elapsed time in the elapsedTime HTML element
                elapsedTimeTag.innerHTML = elapsedTime;

                //2. Stop the recording when the max number of hours is reached
                if (elapsedTimeReachedMaximumNumberOfHours(elapsedTime)) {
                    stopAudioRecording();
                }
            }

            /**
            * @param {String} elapsedTime - elapsed time in the format mm:ss or hh:mm:ss  
            * @returns {Boolean} whether the elapsed time reached the maximum number of hours or not
            */
            function elapsedTimeReachedMaximumNumberOfHours(elapsedTime) {
                //Split the elapsed time by the symbo :
                let elapsedTimeSplitted = elapsedTime.split(":");

                //Turn the maximum recording time in hours to a string and pad it with zero if less than 10
                let maximumRecordingTimeInHoursAsString = maximumRecordingTimeInHours < 10 ? "0" + maximumRecordingTimeInHours : maximumRecordingTimeInHours.toString();

                //if it the elapsed time reach hours and also reach the maximum recording time in hours return true
                if (elapsedTimeSplitted.length === 3 && elapsedTimeSplitted[0] === maximumRecordingTimeInHoursAsString)
                    return true;
                else //otherwise, return false
                    return false;
            }

            /** Computes the elapsedTime since the moment the function is called in the format mm:ss or hh:mm:ss
            * @param {String} startTime - start time to compute the elapsed time since
            * @returns {String} elapsed time in mm:ss format or hh:mm:ss format, if elapsed hours are 0.
            */
            function computeElapsedTime(startTime) {
                //record end time
                let endTime = new Date();

                //time difference in ms
                let timeDiff = endTime - startTime;

                //convert time difference from ms to seconds
                timeDiff = timeDiff / 1000;

                //extract integer seconds that dont form a minute using %
                let seconds = Math.floor(timeDiff % 60); //ignoring uncomplete seconds (floor)

                //pad seconds with a zero if neccessary
                seconds = seconds < 10 ? "0" + seconds : seconds;

                //convert time difference from seconds to minutes using %
                timeDiff = Math.floor(timeDiff / 60);

                //extract integer minutes that don't form an hour using %
                let minutes = timeDiff % 60; //no need to floor possible incomplete minutes, becase they've been handled as seconds
                minutes = minutes < 10 ? "0" + minutes : minutes;

                //convert time difference from minutes to hours
                timeDiff = Math.floor(timeDiff / 60);

                //extract integer hours that don't form a day using %
                let hours = timeDiff % 24; //no need to floor possible incomplete hours, becase they've been handled as seconds

                //convert time difference from hours to days
                timeDiff = Math.floor(timeDiff / 24);

                // the rest of timeDiff is number of days
                let days = timeDiff; //add days to hours

                let totalHours = hours + (days * 24);
                totalHours = totalHours < 10 ? "0" + totalHours : totalHours;

                if (totalHours === "00") {
                    return minutes + ":" + seconds;
                } else {
                    return totalHours + ":" + minutes + ":" + seconds;
                }
            }

            // audio-recording.js ---------------
            //API to handle audio recording 

            var audioRecorder = {
                /** Stores the recorded audio as Blob objects of audio data as the recording continues*/
                audioBlobs: [],/*of type Blob[]*/
                /** Stores the reference of the MediaRecorder instance that handles the MediaStream when recording starts*/
                mediaRecorder: null, /*of type MediaRecorder*/
                /** Stores the reference to the stream currently capturing the audio*/
                streamBeingCaptured: null, /*of type MediaStream*/
                /** Start recording the audio 
                * @returns {Promise} - returns a promise that resolves if audio recording successfully started
                */
                start: function () {
                    //Feature Detection
                    if (!(navigator.mediaDevices && navigator.mediaDevices.getUserMedia)) {
                        //Feature is not supported in browser
                        //return a custom error
                        return Promise.reject(new Error('mediaDevices API or getUserMedia method is not supported in this browser.'));
                    }

                    else {
                        //Feature is supported in browser

                        //create an audio stream
                        return navigator.mediaDevices.getUserMedia({ audio: true }/*of type MediaStreamConstraints*/)
                            //returns a promise that resolves to the audio stream
                            .then(stream /*of type MediaStream*/ => {

                                //save the reference of the stream to be able to stop it when necessary
                                audioRecorder.streamBeingCaptured = stream;

                                //create a media recorder instance by passing that stream into the MediaRecorder constructor
                                audioRecorder.mediaRecorder = new MediaRecorder(stream); /*the MediaRecorder interface of the MediaStream Recording
                                API provides functionality to easily record media*/

                                //clear previously saved audio Blobs, if any
                                audioRecorder.audioBlobs = [];

                                //add a dataavailable event listener in order to store the audio data Blobs when recording
                                audioRecorder.mediaRecorder.addEventListener("dataavailable", event => {
                                    //store audio Blob object
                                    audioRecorder.audioBlobs.push(event.data);
                                });

                                //start the recording by calling the start method on the media recorder
                                audioRecorder.mediaRecorder.start();
                            });

                        /* errors are not handled in the API because if its handled and the promise is chained, the .then after the catch will be executed*/
                    }
                },
                /** Stop the started audio recording
                * @returns {Promise} - returns a promise that resolves to the audio as a blob file
                */
                stop: function () {
                    //return a promise that would return the blob or URL of the recording
                    return new Promise(resolve => {
                        //save audio type to pass to set the Blob type
                        let mimeType = audioRecorder.mediaRecorder.mimeType;

                        //listen to the stop event in order to create & return a single Blob object
                        audioRecorder.mediaRecorder.addEventListener("stop", () => {
                            //create a single blob object, as we might have gathered a few Blob objects that needs to be joined as one
                            let audioBlob = new Blob(audioRecorder.audioBlobs, { type: mimeType });
                            
                            //resolve promise with the single audio blob representing the recorded audio
                            resolve(audioBlob);
                        });
                        audioRecorder.cancel();
                    });
                },
                /** Cancel audio recording*/
                cancel: function () {
                    //stop the recording feature
                    audioRecorder.mediaRecorder.stop();

                    //stop all the tracks on the active stream in order to stop the stream
                    audioRecorder.stopStream();

                    //reset API properties for next recording
                    audioRecorder.resetRecordingProperties();
                },
                /** Stop all the tracks on the active stream in order to stop the stream and remove
                * the red flashing dot showing in the tab
                */
                stopStream: function () {
                    //stopping the capturing request by stopping all the tracks on the active stream
                    audioRecorder.streamBeingCaptured.getTracks() //get all tracks from the stream
                        .forEach(track /*of type MediaStreamTrack*/ => track.stop()); //stop each one
                },
                /** Reset all the recording properties including the media recorder and stream being captured*/
                resetRecordingProperties: function () {
                    audioRecorder.mediaRecorder = null;
                    audioRecorder.streamBeingCaptured = null;

                    /*No need to remove event listeners attached to mediaRecorder as
                    If a DOM element which is removed is reference-free (no references pointing to it), the element itself is picked
                    up by the garbage collector as well as any event handlers/listeners associated with it.
                    getEventListeners(audioRecorder.mediaRecorder) will return an empty array of events.*/
                }
            }

            startAudioRecording();
        },
    },

    mounted() {

    }
}
</script>

<style>

/* style.css*/

/* Media Queries */

/* Small Devices*/

@media (min-width: 0px) {
    * {
        box-sizing: border-box;
    }
    .audio-recording-container {
        width: 100%;
        height: 20vh;
        /* view port height*/
        /*targeting Chrome & Safari*/
        display: -webkit-flex;
        /*targeting IE10*/
        display: -ms-flex;
        display: flex;
        flex-direction: column;
        justify-content: center;
        /*horizontal centering*/
        align-items: center;
    }
    .start-recording-button {
        font-size: 70px;
        color: #435f7a;
        cursor: pointer;
        opacity: .5;
        margin-bottom: 30px;
    }
    .start-recording-button:hover {
        opacity: 1;
    }
    .recording-contorl-buttons-container {
        /*targeting Chrome & Safari*/
        display: -webkit-flex;
        /*targeting IE10*/
        display: -ms-flex;
        display: flex;
        justify-content: space-evenly;
        /*horizontal centering*/
        align-items: center;
        width: 334px;
        margin-bottom: 30px;
    }
    .cancel-recording-button,
    .stop-recording-button {
        font-size: 70px;
        cursor: pointer;
    }
    .cancel-recording-button {
        color: red;
        opacity: 0.7;
    }
    .cancel-recording-button:hover {
        color: rgb(206, 4, 4);
    }
    .stop-recording-button {
        color: #33cc33;
        opacity: 0.7;
    }
    .stop-recording-button:hover {
        color: #27a527;
    }
    .recording-elapsed-time {
        /*targeting Chrome & Safari*/
        display: -webkit-flex;
        /*targeting IE10*/
        display: -ms-flex;
        display: flex;
        justify-content: center;
        /*horizontal centering*/
        align-items: center;
    }
    .red-recording-dot {
        font-size: 25px;
        color: red;
        margin-right: 12px;
        /*transitions with Firefox, IE and Opera Support browser support*/
        animation-name: flashing-recording-dot;
        -webkit-animation-name: flashing-recording-dot;
        -moz-animation-name: flashing-recording-dot;
        -o-animation-name: flashing-recording-dot;
        animation-duration: 2s;
        -webkit-animation-duration: 2s;
        -moz-animation-duration: 2s;
        -o-animation-duration: 2s;
        animation-iteration-count: infinite;
        -webkit-animation-iteration-count: infinite;
        -moz-animation-iteration-count: infinite;
        -o-animation-iteration-count: infinite;
    }
    /* The animation code */
    @keyframes flashing-recording-dot {
        0% {
            opacity: 1;
        }
        50% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }
    @-webkit-keyframes flashing-recording-dot {
        0% {
            opacity: 1;
        }
        50% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }
    @-moz-keyframes flashing-recording-dot {
        0% {
            opacity: 1;
        }
        50% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }
    @-o-keyframes flashing-recording-dot {
        0% {
            opacity: 1;
        }
        50% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }
    .elapsed-time {
        font-size: 32px;
    }
    .recording-contorl-buttons-container.hide {
        display: none;
    }
    .overlay {
        position: absolute;
        top: 0;
        height: 100vh;
        width: 100%;
        background-color: rgba(82, 76, 76, 0.35);
        /*targeting Chrome & Safari*/
        display: -webkit-flex;
        /*targeting IE10*/
        display: -ms-flex;
        display: flex;
        justify-content: center;
        /*horizontal centering*/
        align-items: center;
    }
    .overlay.hide {
        display: none;
    }
    .browser-not-supporting-audio-recording-box {
        /*targeting Chrome & Safari*/
        display: -webkit-flex;
        /*targeting IE10*/
        display: -ms-flex;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        /*horizontal centering*/
        align-items: center;
        width: 317px;
        height: 119px;
        background-color: white;
        border-radius: 10px;
        padding: 15px;
        font-size: 16px;
    }
    .close-browser-not-supported-box {
        cursor: pointer;
        background-color: #abc1c05c;
        border-radius: 10px;
        font-size: 16px;
        border: none;
    }
    .close-browser-not-supported-box:hover {
        background-color: #92a5a45c;
    }
    .close-browser-not-supported-box:focus {
        outline: none;
        border: none;
    }
    .audio-element.hide {
        display: none;
    }
    .text-indication-of-audio-playing-container {
        height: 20px;
    }
    .text-indication-of-audio-playing {
        font-size: 20px;
    }
    .text-indication-of-audio-playing.hide {
        display: none;
    }
    /* 3 Dots animation*/
    .text-indication-of-audio-playing span {
        /*transitions with Firefox, IE and Opera Support browser support*/
        animation-name: blinking-dot;
        -webkit-animation-name: blinking-dot;
        -moz-animation-name: blinking-dot;
        -o-animation-name: blinking-dot;
        animation-duration: 2s;
        -webkit-animation-duration: 2s;
        -moz-animation-duration: 2s;
        -o-animation-duration: 2s;
        animation-iteration-count: infinite;
        -webkit-animation-iteration-count: infinite;
        -moz-animation-iteration-count: infinite;
        -o-animation-iteration-count: infinite;
    }
    .text-indication-of-audio-playing span:nth-child(2) {
        animation-delay: .4s;
        -webkit-animation-delay: .4s;
        -moz-animation-delay: .4s;
        -o-animation-delay: .4s;
    }
    .text-indication-of-audio-playing span:nth-child(3) {
        animation-delay: .8s;
        -webkit-animation-delay: .8s;
        -moz-animation-delay: .8s;
        -o-animation-delay: .8s;
    }
    /* The animation code */
    @keyframes blinking-dot {
        0% {
            opacity: 0;
        }
        50% {
            opacity: 1;
        }
        100% {
            opacity: 0;
        }
    }
    /* The animation code */
    @-webkit-keyframes blinking-dot {
        0% {
            opacity: 0;
        }
        50% {
            opacity: 1;
        }
        100% {
            opacity: 0;
        }
    }
    /* The animation code */
    @-moz-keyframes blinking-dot {
        0% {
            opacity: 0;
        }
        50% {
            opacity: 1;
        }
        100% {
            opacity: 0;
        }
    }
    /* The animation code */
    @-o-keyframes blinking-dot {
        0% {
            opacity: 0;
        }
        50% {
            opacity: 1;
        }
        100% {
            opacity: 0;
        }
    }
}

/* Medium devices */

@media (min-width: 768px) {}

/* Large devices */

@media (min-width: 992px) {}

/*Ipad pro view*/

/* 
  @media (min-width: 1024px) {
  
  } */

/* Extra Large devices */

@media (min-width: 1200px) {}


</style>
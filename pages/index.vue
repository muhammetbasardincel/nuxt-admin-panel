<template>
    <div class="w-screen h-screen flex overflow-hidden">
        <!--    Side Bar -->
        <div :class="{ 'hidden': !showSideBar}"  class="min-w-[250px] lg:w-[320px] h-full bg-gray-200 text-white lg:block transition-transform duration-300 ease-out transform z-40">
            <div class="h-[50px] bg-gray-900 flex justify-start items-center">
                <div class="px-[20px]">
                    <h3 class="font-bold text-xl">Admin Panel</h3>
                </div>
            </div>
            <div class="h-[calc(100vh-150px)] bg-gray-800 py-[20px]">
                <!--            <div class="flex flex-col justify-between h-full bg-red-400"></div>-->
                <div class="px-[10px] flex flex-col space-y-[10px] h-full">
                    <div class="h-full overflow-auto space-y-1">
                        <a href="" class="inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25" />
                            </svg>

                            Giriş
                        </a>


                        <div @click="dropdown('yazilar')"  class="cursor-pointer inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 00-9-9z" />
                            </svg>
                            Yazılar
                        </div>
                        <div v-if="dropdownName=='yazilar'" class="bg-gray-700 space-y-1 rounded">
                            <a href="" class="pl-11 inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                                <!--                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">-->
                                <!--                                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 00-9-9z" />-->
                                <!--                            </svg>-->
                                Yazı Ekle
                            </a>
                            <a href="" class="pl-11 inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                                <!--                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">-->
                                <!--                                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 00-9-9z" />-->
                                <!--                            </svg>-->
                                Yazılar
                            </a>
                        </div>


                        <a href="" class="inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px] flex justify-center">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M9.568 3H5.25A2.25 2.25 0 003 5.25v4.318c0 .597.237 1.17.659 1.591l9.581 9.581c.699.699 1.78.872 2.607.33a18.095 18.095 0 005.223-5.223c.542-.827.369-1.908-.33-2.607L11.16 3.66A2.25 2.25 0 009.568 3z" />
                                <path stroke-linecap="round" stroke-linejoin="round" d="M6 6h.008v.008H6V6z" />
                            </svg>
                            Kategoriler
                        </a>

                        <a href="" class="inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px] ">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M11.35 3.836c-.065.21-.1.433-.1.664 0 .414.336.75.75.75h4.5a.75.75 0 00.75-.75 2.25 2.25 0 00-.1-.664m-5.8 0A2.251 2.251 0 0113.5 2.25H15c1.012 0 1.867.668 2.15 1.586m-5.8 0c-.376.023-.75.05-1.124.08C9.095 4.01 8.25 4.973 8.25 6.108V8.25m8.9-4.414c.376.023.75.05 1.124.08 1.131.094 1.976 1.057 1.976 2.192V16.5A2.25 2.25 0 0118 18.75h-2.25m-7.5-10.5H4.875c-.621 0-1.125.504-1.125 1.125v11.25c0 .621.504 1.125 1.125 1.125h9.75c.621 0 1.125-.504 1.125-1.125V18.75m-7.5-10.5h6.375c.621 0 1.125.504 1.125 1.125v9.375m-8.25-3l1.5 1.5 3-3.75" />
                            </svg>
                            Sayfalar
                        </a>
                        <a href="" class="inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 15.75l5.159-5.159a2.25 2.25 0 013.182 0l5.159 5.159m-1.5-1.5l1.409-1.409a2.25 2.25 0 013.182 0l2.909 2.909m-18 3.75h16.5a1.5 1.5 0 001.5-1.5V6a1.5 1.5 0 00-1.5-1.5H3.75A1.5 1.5 0 002.25 6v12a1.5 1.5 0 001.5 1.5zm10.5-11.25h.008v.008h-.008V8.25zm.375 0a.375.375 0 11-.75 0 .375.375 0 01.75 0z" />
                            </svg>

                            Görseller
                        </a>
                        <a href="" class="inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px] ">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M15 19.128a9.38 9.38 0 002.625.372 9.337 9.337 0 004.121-.952 4.125 4.125 0 00-7.533-2.493M15 19.128v-.003c0-1.113-.285-2.16-.786-3.07M15 19.128v.106A12.318 12.318 0 018.624 21c-2.331 0-4.512-.645-6.374-1.766l-.001-.109a6.375 6.375 0 0111.964-3.07M12 6.375a3.375 3.375 0 11-6.75 0 3.375 3.375 0 016.75 0zm8.25 2.25a2.625 2.625 0 11-5.25 0 2.625 2.625 0 015.25 0z" />
                            </svg>

                            Kullanıcılar
                        </a>

                        <a href="" class="inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
                            </svg>

                            Eposta
                        </a>
                        <a href="" class="inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M10.5 6a7.5 7.5 0 107.5 7.5h-7.5V6z" />
                                <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 10.5H21A7.5 7.5 0 0013.5 3v7.5z" />
                            </svg>

                            Raporlar
                        </a>

                        <div @click="dropdown('ayarlar')" class=" cursor-pointer inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px] flex justify-center">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12a7.5 7.5 0 0015 0m-15 0a7.5 7.5 0 1115 0m-15 0H3m16.5 0H21m-1.5 0H12m-8.457 3.077l1.41-.513m14.095-5.13l1.41-.513M5.106 17.785l1.15-.964m11.49-9.642l1.149-.964M7.501 19.795l.75-1.3m7.5-12.99l.75-1.3m-6.063 16.658l.26-1.477m2.605-14.772l.26-1.477m0 17.726l-.26-1.477M10.698 4.614l-.26-1.477M16.5 19.794l-.75-1.299M7.5 4.205L12 12m6.894 5.785l-1.149-.964M6.256 7.178l-1.15-.964m15.352 8.864l-1.41-.513M4.954 9.435l-1.41-.514M12.002 12l-3.75 6.495" />
                            </svg>
                            Ayarlar
                        </div>
                        <div v-if="dropdownName=='ayarlar'" class="bg-gray-700 space-y-1 rounded">
                            <a href="" class="pl-11 inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                                <!--                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">-->
                                <!--                                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 00-9-9z" />-->
                                <!--                            </svg>-->
                                Site Ayarları
                            </a>
                            <a href="" class="pl-11 inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                                <!--                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">-->
                                <!--                                <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 00-9-9z" />-->
                                <!--                            </svg>-->
                                İletişim Ayarları
                            </a>
                        </div>

                        <a href="" class="inline-flex relative items-center py-[10px] px-[10px] w-full font-medium rounded-md text-white border-gray-200 hover:bg-gray-200 hover:text-gray-800 transition duration-300 ease-in-out ">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="mr-2 w-[25px] h-[25px]">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M12 6v6h4.5m4.5 0a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                            Lisans
                        </a>


                    </div>

                    <!--                <div class="h-[50px]">-->
                    <!--                    <a href="" class="inline-flex relative items-center py-[10px] px-[10px] w-full text-white hover:bg-white hover:text-black rounded-xl">-->
                    <!--                        <svg id="Icons" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" class="mr-2 w-[25px] h-[25px] fill-current flex justify-center">-->
                    <!--                            <path class="cls-1" d="M23.588,8.191l-11-8a1,1,0,0,0-1.176,0l-11,8A1,1,0,0,0,1.588,9.809L3,8.782V21a2.006,2.006,0,0,0,2,2H9V14a1,1,0,0,1,1-1h4a1,1,0,0,1,1,1v9h4a2.006,2.006,0,0,0,2-2V8.782l1.412,1.027a1,1,0,1,0,1.176-1.618Z"/>-->
                    <!--                        </svg>-->
                    <!--                        Setting-->
                    <!--                    </a>-->
                    <!--                </div>-->
                    <!--                <div class="h-[70px]">-->
                    <!--                    <div class="bg-slate-700 w-full h-[2px] block mb-1"></div>-->
                    <!--                    <h1 class="text-slate-300 font-semibold">Lisans Süresi</h1>-->
                    <!--                    <div v-if="!isExpired" class="my-1">-->
                    <!--                        <div class="w-full bg-gray-200 rounded-lg">-->
                    <!--                            <div class="bg-lime-500 text-xs leading-none py-1 text-center text-white rounded-lg" :style="'width: ' + elapsedPercentage + '%'">-->
                    <!--                                {{ elapsedPercentage }}%-->
                    <!--                            </div>-->
                    <!--                        </div>-->
                    <!--                    </div>-->
                    <!--                    <div v-if="isExpired">-->
                    <!--                        <h1 class="text-red-600">Abonelik süreniz doldu.</h1>-->
                    <!--                        <button class="bg-lime-500 rounded py-1 px-2 text-teal-900 hover:bg-lime-600">Lisans Satın Al</button>-->
                    <!--                    </div>-->
                    <!--                    <h1 v-else class="text-xs text-slate-200">Kalan: {{ remainingTime }}</h1>-->

                    <!--                </div>-->
                </div>
            </div>
            <div class="h-[100px] bg-gray-800 border-t-2 pt-3 border-slate-700">
                <div class="px-[15px]">
                    <h1 class="text-slate-300 font-semibold">Lisans Süresi</h1>
                    <div v-if="!isExpired" class="my-1">
                        <div class="w-full bg-gray-200 rounded-lg">
                            <div class="bg-lime-500 text-xs leading-none py-1 text-center text-white rounded-lg" :style="'width: ' + elapsedPercentage + '%'">
                                {{ elapsedPercentage }}%
                            </div>
                        </div>
                    </div>
                    <div v-if="isExpired">
                        <h1 class="text-red-600">Abonelik süreniz doldu.</h1>
                        <button class="bg-lime-500 rounded py-1 px-2 text-teal-900 hover:bg-lime-600">Lisans Satın Al</button>
                    </div>
                    <h1 v-else class="text-xs text-slate-200">Kalan: {{ remainingTime }}</h1>
                </div>
            </div>
        </div>

        <!--    Maim -->
        <div class="w-full h-full bg-gray-400">
            <div class="h-[50px] bg-gray-100 shadow-sm z-10 flex items-center border-b px-[20px]">
                <div v-on:touchstart="toggleSideBar"  @touchstart="toggleSideBar" @click="toggleSideBar" class="lg:hidden cursor-pointer w-[30px] flex justify-center items-center">
                    <svg class="w-[25px] h-[25px]" style="enable-background:new 0 0 32 32;" version="1.1" viewBox="0 0 32 32" width="32px" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                    <path d="M4,10h24c1.104,0,2-0.896,2-2s-0.896-2-2-2H4C2.896,6,2,6.896,2,8S2.896,10,4,10z M28,14H4c-1.104,0-2,0.896-2,2  s0.896,2,2,2h24c1.104,0,2-0.896,2-2S29.104,14,28,14z M28,22H4c-1.104,0-2,0.896-2,2s0.896,2,2,2h24c1.104,0,2-0.896,2-2  S29.104,22,28,22z"/>
                </svg>
                </div>

                <!-- Main Bar  -->
                <div class="w-[calc(100%-30px)] lg:w-full flex space-x-3">

                    <!-- Main Heeader               -->
                    <div class="w-[calc(100%-160px)] lg:w-[calc(100%-200px)] flex items-center justify-start">
                        Hoşgeldiniz...
                    </div>


                    <!-- Inbox -->
                    <div class="w-10 relative">
                        <div class="w-10 h-10 flex justify-center items-center rounded-lg hover:bg-slate-50 hover:shadow-md cursor-pointer py-1 px-1">
                            <!--                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-7 h-7">-->
                            <!--                            <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 13.5h3.86a2.25 2.25 0 012.012 1.244l.256.512a2.25 2.25 0 002.013 1.244h3.218a2.25 2.25 0 002.013-1.244l.256-.512a2.25 2.25 0 012.013-1.244h3.859m-19.5.338V18a2.25 2.25 0 002.25 2.25h15A2.25 2.25 0 0021.75 18v-4.162c0-.224-.034-.447-.1-.661L19.24 5.338a2.25 2.25 0 00-2.15-1.588H6.911a2.25 2.25 0 00-2.15 1.588L2.35 13.177a2.25 2.25 0 00-.1.661z" />-->
                            <!--                        </svg>-->
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25h-15a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5h-15a2.25 2.25 0 00-2.25 2.25m19.5 0v.243a2.25 2.25 0 01-1.07 1.916l-7.5 4.615a2.25 2.25 0 01-2.36 0L3.32 8.91a2.25 2.25 0 01-1.07-1.916V6.75" />
                            </svg>

                            <span class="text-red-700 text-2xl bg-red-700 rounded-full block w-2 h-2 hidden"></span>
                        </div>
                    </div>
                    <!-- Notification -->
                    <div class="w-10 relative">

                        <div class="w-10 h-10 flex justify-center items-center rounded-lg hover:bg-slate-50 hover:shadow-md cursor-pointer py-1 px-1">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0" />
                            </svg>
                            <span class="text-red-700 text-2xl bg-red-700 rounded-full block w-2 h-2"></span>
                        </div>
                    </div>
                    <!-- User login -->
                    <div class="lg:w-[200px] w-10">
                        <div @click="toggleDrop" v-on:touchstart="toggleDrop"  @touchstart="toggleDrop" class="flex items-center justify-start space-x-4 cursor-pointer">
                            <img class="w-10 h-10 rounded-full border-2 border-gray-50" src="/profil.jpg" alt="" >
                            <div class="font-semibold dark:text-blue-950 text-left text-white hidden lg:block">
                                <div>Başar Dinçel</div>
                                <div class="text-xs text-gray-500 dark:text-gray-400">Yönetici</div>
                            </div>
                        </div>
                        <div v-on:mouseleave="toggleDrop" v-show="showDropDown" class="absolute right-[10px] z-10 mt-2 w-56 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="menu-button" tabindex="-1">
                            <div class="py-1 text-left">
                                <a href="" class="text-gray-700 block px-4 py-2 text-sm">Profil</a>
                                <a href="" class="text-gray-700 block px-4 py-2 text-sm">Şifre</a>
                                <a href="" class="text-gray-700 block px-4 py-2 text-sm">Ayarlar</a>
                                <hr>
                                <a href="" class="text-gray-700 block px-4 py-2 text-sm">Çıkış Yap</a>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
            <div class="h-[calc(100vh-50px)] bg-gray-50 p-[20px]">
                <div class="border border-gray-300 rounded-md p-[20px] h-full overflow-auto" style="-webkit-overflow-scrolling: touch">
                    İçerikler gelecek
                </div>
            </div>
        </div>

    </div>
</template>

<script setup>
const showDropDown = ref(false)
const showSideBar = ref(false)
let dropdownName = useState('dropdownName')
const isExpired = ref("")
const remainingTime = ref("")
const elapsedPercentage = ref("")
function dropdown(value){
    dropdownName.value === value ? dropdownName.value = '' : dropdownName.value = value
}
onMounted(()=>{
    const startDate = new Date('2023-04-15 00:00:00');
    const endDate = new Date('2023-06-11 13:59:59');
    const result = calculateSubscriptionUsage0(startDate, endDate);
    let cevap = JSON.parse(result)
    isExpired.value = cevap.isExpired
    elapsedPercentage.value = cevap.elapsedPercentage
    remainingTime.value= cevap.remainingTime
})
function toggleDrop(){
    showDropDown.value = !showDropDown.value
}

function toggleSideBar(){
    showSideBar.value = !showSideBar.value
}
function calculateSubscriptionUsage0(startDate, endDate) {
    const currentTime = new Date();
    const totalSeconds = (endDate - startDate) / 1000;
    const remainingSeconds = (endDate - currentTime) / 1000;
    const elapsedSeconds = totalSeconds - remainingSeconds;

    let remainingTime = '';
    let elapsedPercentage = 0;

    if (remainingSeconds <= 0) {
        remainingTime = 'Expired';
    } else {
        const days = Math.floor(remainingSeconds / 86400);
        const hours = Math.floor((remainingSeconds % 86400) / 3600);
        const minutes = Math.floor((remainingSeconds % 3600) / 60);
        const seconds = Math.floor(remainingSeconds % 60);

        remainingTime = `${days > 0 ? days + ' gün ' : ''}${hours > 0 ? hours + ' saat ' : ''}${minutes > 0 ? minutes + ' dakika ' : ''}${seconds > 0 ? seconds + ' saniye ' : ''}`;
    }

    let result;
    if (remainingSeconds <= 0) {
        result = {
            remainingTime,
            isExpired: true
        };
    } else {
        if (totalSeconds > 0) {
            elapsedPercentage = Math.round(elapsedSeconds / totalSeconds * 100);
        }
        result = {
            remainingTime: remainingTime.trim(),
            elapsedPercentage,
            isExpired: false
        };
    }

    return JSON.stringify(result);
}

</script>

<style scoped>

</style>
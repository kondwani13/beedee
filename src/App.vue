<template>
<header class="z-10 bg-gray-900 sm:flex sm:justify-between sm:items-center sm:px-4 sm:py-3 ">
    <div class="flex items-center justify-between px-4 py-3 sm:p-0">
      <div class="pr-8">
        <router-link to="/"><img class="h-12 px-2" src="./images/logos.png" alt="logo"></router-link>
      </div>
      <div class="sm:hidden">
        <button @click="isOpen = !isOpen" type="button" class="block text-gray-200 hover:text-white focus:text-white focus:outline-none">
          <svg class="h-6 w-6 fill-current" viewBox="0 0 24 24">
            <path v-if="isOpen" fill-rule="evenodd" d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"/>
            <path v-if="!isOpen" fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"/>
          </svg>
        </button>
      </div>
    </div>
    <nav id="nav" :class="isOpen ? 'block' : 'hidden'" class="px-3 pt-2 pb-4 sm:flex sm:p-0">
      <router-link to="/" class="block px-2 py-1 text-white font-semibold rounded hover:bg-gray-800" >Home</router-link>
      <router-link to="/services" class="mt-1 block px-2 py-1 text-white font-semibold rounded hover:bg-gray-800 sm:mt-0 sm:ml-2">Services</router-link>

      <router-link to="/about" class="mt-1 block px-2 py-1 text-white font-semibold rounded hover:bg-gray-800 sm:mt-0 sm:ml-2">About</router-link>
      <router-link to="/contact" class="mt-1 block px-2 py-1 text-white font-semibold rounded hover:bg-gray-800 sm:mt-0 sm:ml-2">Contact</router-link>

    </nav>
  </header>
  <router-view/>

  <footer class="pb-0 bg-gray-800">
        <div class="w-full border-gray-300 border-t lg:w-11/12 md:w-11/12 lg:mx-auto md:mx-auto">
            <div class="container mx-auto py-12">
                <div class="xl:flex lg:flex md:flex pt-6">
                    <div class="w-11/12 xl:w-3/6 lg:w-2/5 mx-auto lg:mx-0 xl:mx-0">
                        <div class="w-2/5">
                             <router-link to="/"><img src="@/images/logos.png" alt="log"></router-link>
                        </div>
                    </div>
                    <div class="w-11/12 xl:w-1/6 lg:w-2/5 mx-auto lg:mx-0 xl:mx-0 pt-3 xl:flex xl:justify-end pl-3 sm:pl-0">
                        <ul>
                            <li class="text-white font-bold text-xl mb-6">About us</li>
                            <li class="text-base text-white hover:text-purple-600 mb-5">
                                <router-link to="/about">About</router-link>
                            </li>
                           
                            <li class="text-base text-white hover:text-purple-600 mb-5">
                                <router-link @click="$scrollToMiddle" to="/faq">Our team</router-link>
                            </li>
                            <li class="text-base text-white hover:text-purple-600 mb-5">
                                <a href="javascript:void(0)">Achievements</a>
                            </li>
                        </ul>
                    </div>
                    <div class="w-11/12 xl:w-1/6 lg:w-2/5 mx-auto lg:mx-0 xl:mx-0 pt-3 xl:flex xl:justify-end pl-3 sm:pl-0">
                        <ul>
                            <li class="text-white font-bold text-xl mb-6">Support</li>
                            <li class="text-base text-white hover:text-purple-600 mb-5">
                                <router-link to="/faq">Help centre</router-link>
                            </li>
                            
                            
                            <li class="text-base text-white hover:text-purple-600 mb-5">
                                <router-link to="/contact">Contact</router-link>
                            </li>
                           
                            
                        </ul>
                    </div>
                    <div class="w-11/12 xl:w-1/6 lg:w-2/5 mx-auto lg:mx-0 xl:mx-0 pt-3 xl:flex xl:justify-end pl-3 sm:pl-0">
                        <ul>
                            <li class="text-white font-bold text-xl mb-6">Resources</li>
                            <li class="text-base text-white hover:text-purple-600 mb-5">
                                <a href="javascript:void(0)">Accessibility</a>
                            </li>
                           
                            
                            
                        
                            
                        </ul>
                    </div>
                </div>
                <div class="xl:flex flex-wrap justify-between xl:mt-24 mt-16 pb-6 pl-3 sm:pl-0">
                    <div class="w-11/12 xl:w-2/6 mx-auto lg:mx-0 xl:mx-0 mb-6 xl:mb-0">
                        <p class="text-white text-base">2021 BeeDee. All Rights Reserved</p>
                    </div>
                    <div class="w-11/12 xl:w-2/6 mx-auto lg:mx-0 xl:mx-0 mb-6 lg:mb-0 xl:mb-0">
                        <ul class="xl:flex lg:flex md:flex sm:flex justify-between">
                            <li class="text-white hover:text-purple-600 text-base mb-4 sm:mb-0">
                                <router-link to="/terms-of-service">Terms of service</router-link>
                            </li>
                            <li class="text-white hover:text-purple-600 text-base mb-4 sm:mb-0">
                                <router-link to="/privacy-policy">Privacy Policy</router-link>
                            </li>
                            <li class="text-white hover:text-purple-600 text-base mb-4 sm:mb-0">
                                <a href="javascript:void(0)">Security</a>
                            </li>
                            <li class="text-white hover:text-purple-600 text-base mb-4 sm:mb-0">
                                <a href="javascript:void(0)">Sitemap</a>
                            </li>
                        </ul>
                    </div>
                    <div class="w-11/12 xl:w-1/6 lg:w-1/6 sm:w-11/12 mx-auto lg:mx-0 xl:mx-0 mb-6 lg:mb-0 xl:mb-0 mt-8 lg:mt-8 xl:mt-0">
                        <div class="flex justify-start sm:justify-start xl:justify-end space-x-6 pr-2 xl:pr-0 lg:pr-0 md:pr-0 sm:pr-0">
                            <div>
                                <a href="javascript:void(0)">
                                    <svg aria-label="Twitter" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#718096" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="feather feather-twitter">
                                        <path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"></path>
                                    </svg>
                                </a>
                            </div>
                            <div>
                                <a href="javascript:void(0)">
                                    <svg aria-label="Instagram" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#718096" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="feather feather-instagram">
                                        <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
                                        <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
                                        <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
                                    </svg>
                                </a>
                            </div>
                            <div>
                                <a href="javascript:void(0)">
                                    <svg aria-label="Dribble" xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-dribbble" width="24" height="24" viewBox="0 0 24 24" stroke-width="1.5" stroke="#718096" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" />
                                        <circle cx="12" cy="12" r="9" />
                                        <path d="M9 3.6c5 6 7 10.5 7.5 16.2" />
                                        <path d="M6.4 19c3.5-3.5 6-6.5 14.5-6.4" />
                                        <path d="M3.1 10.75c5 0 9.814-.38 15.314-5" />
                                    </svg>
                                </a>
                            </div>
                            <div>
                                <a href="javascript:void(0)">
                                    <svg aria-label="Github" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#718096" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="feather feather-github">
                                        <path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path>
                                    </svg>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
  

  
  
</template>
<script>
export default {
 name: "app",
 components: {

 },
  data() {
    return {
      isOpen: false,
    }
  },
}
</script>

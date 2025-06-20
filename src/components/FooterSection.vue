<template>
    <section id="footer" class="bg-black text-white pt-16 px-6">
        <div class="max-w-7xl mx-auto grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-12 pb-10">
            <!-- Newsletter -->
            <div>
                <h3 class="text-3xl font-rollie mb-6">Newsletter</h3>
                <div class="space-y-4">
                    <input type="email" placeholder="Email Address"
                        class="w-full bg-transparent border-b border-white placeholder-gray-300 focus:outline-none py-2" />
                    <input type="text" placeholder="First Name"
                        class="w-full bg-transparent border-b border-white placeholder-gray-300 focus:outline-none py-2" />
                    <input type="text" placeholder="Last Name"
                        class="w-full bg-transparent border-b border-white placeholder-gray-300 focus:outline-none py-2" />
                    <input type="text" placeholder="Phone Number"
                        class="w-full bg-transparent border-b border-white placeholder-gray-300 focus:outline-none py-2" />
                </div>

                <h4 class="mt-6 text-sm font-semibold">Marketing Permissions</h4>
                <div class="flex flex-col space-y-2 mt-2 text-sm">
                    <label class="flex items-center space-x-2">
                        <input type="checkbox" class="form-checkbox text-black" />
                        <span>Email</span>
                    </label>
                    <label class="flex items-center space-x-2">
                        <input type="checkbox" class="form-checkbox text-black" />
                        <span>SMS</span>
                    </label>
                </div>

                <p class="text-xs text-gray-400 mt-4">
                    By signing up you agree to receive the latest news and exclusive offers from our restaurants.
                </p>

                <button
                    class="mt-6 bg-white text-black px-6 py-2 rounded-full font-cromlin hover:bg-gray-200 transition">
                    Subscribe
                </button>
            </div>

            <!-- Menu Links -->
            <div>
                <ul class="space-y-3 text-base text-gray-300 font-corporate">
                    <li><a href="#" class="hover:text-white transition">Signature Cakes</a></li>
                    <li><a href="#" class="hover:text-white transition">Bespoke Cakes</a></li>
                    <li><a href="#" class="hover:text-white transition">Wedding Cakes</a></li>
                    <li><a href="#" class="hover:text-white transition">Cakesicles</a></li>
                    <li><a href="#" class="hover:text-white transition">Chocolates</a></li>
                    <li><a href="#" class="hover:text-white transition">Master Classes</a></li>
                </ul>
            </div>

            <!-- Support Links -->
            <div>
                <ul class="space-y-3 text-base text-gray-300 font-corporate">
                    <li><a href="#" class="hover:text-white transition">Payment and Delivery</a></li>
                    <li><a href="#" class="hover:text-white transition">Help Center</a></li>
                    <li><a href="#" class="hover:text-white transition">FAQs</a></li>
                    <li><a href="#" class="hover:text-white transition">Contact Us</a></li>
                </ul>

                <!-- Social Media Icons -->
                <div class="flex space-x-5 mt-6">
                    <!-- TikTok -->
                    <a href="#" class="bg-white text-black p-3 rounded-full hover:bg-black hover:text-white transition">
                        <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" viewBox="0 0 448 512"
                            fill="currentColor">
                            <path
                                d="M448 209.9a210.1 210.1 0 0 1 -122.8-39.3V349.4A162.6 162.6 0 1 1 185 188.3V278.2a74.6 74.6 0 1 0 52.2 71.2V0l88 0a121.2 121.2 0 0 0 1.9 22.2h0A122.2 122.2 0 0 0 381 102.4a121.4 121.4 0 0 0 67 20.1z" />
                        </svg>
                    </a>

                    <!-- YouTube -->
                    <a href="#" class="bg-white text-black p-3 rounded-full hover:bg-black hover:text-white transition">
                        <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" viewBox="0 0 576 512"
                            fill="currentColor">
                            <path
                                d="M549.7 124.1c-6.3-23.7-24.8-42.3-48.3-48.6C458.8 64 288 64 288 64S117.2 64 74.6 75.5c-23.5 6.3-42 24.9-48.3 48.6-11.4 42.9-11.4 132.3-11.4 132.3s0 89.4 11.4 132.3c6.3 23.7 24.8 41.5 48.3 47.8C117.2 448 288 448 288 448s170.8 0 213.4-11.5c23.5-6.3 42-24.2 48.3-47.8 11.4-42.9 11.4-132.3 11.4-132.3s0-89.4-11.4-132.3zm-317.5 213.5V175.2l142.7 81.2-142.7 81.2z" />
                        </svg>
                    </a>

                    <!-- Facebook -->
                    <a href="#" class="bg-white text-black p-3 rounded-full hover:bg-black hover:text-white transition">
                        <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" viewBox="0 0 320 512"
                            fill="currentColor">
                            <path
                                d="M80 299.3V512H196V299.3h86.5l18-97.8H196V166.9c0-51.7 20.3-71.5 72.7-71.5c16.3 0 29.4 .4 37 1.2V7.9C291.4 4 256.4 0 236.2 0C129.3 0 80 50.5 80 159.4v42.1H14v97.8H80z" />
                        </svg>
                    </a>

                    <!-- Instagram -->
                    <a href="#" class="bg-white text-black p-3 rounded-full hover:bg-black hover:text-white transition">
                        <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" viewBox="0 0 448 512"
                            fill="currentColor">
                            <path
                                d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z" />
                        </svg>
                    </a>
                </div>

                <!-- Payment Methods -->
                <div class="flex justify-start items-center space-x-1 bg-white rounded-full mt-6 w-60">
                    <div v-for="(payment, index) in paymentMethods" :key="index"
                        class="h-10 w-16 bg-contain bg-no-repeat bg-center"
                        :style="{ backgroundImage: `url(${payment})` }"></div>
                </div>

            </div>
        </div>

        <!-- Bottom Footer Bar -->
        <div class="text-center py-6 text-sm text-gray-400 ">
            © 2023 The Cake Boutique. All rights reserved.
        </div>
    </section>
</template>

<script>
import visa from "../assets/visa.png"
import masterCard from "../assets/mastercard.png"
import americanExpress from "../assets/american-express.png"
import paypal from "../assets/paypal.png"
export default {
    name: "FooterSection",
    data() {
        return {
            paymentMethods: [
                visa,
                masterCard,
                americanExpress,
                paypal
            ]
        }
    }
};
</script>

<style scoped>
input[type="checkbox"] {
    accent-color: white;
}
</style>

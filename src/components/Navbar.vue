<template>
    <nav :class="[
        'w-full fixed top-0 left-0 z-50 text-white transition duration-300',
        scrolled ? 'backdrop-blur-md bg-black/40' : 'bg-transparent'
    ]">
        <div class="flex justify-between space-x-6 items-center mx-6 sm:mx-12 text-center sm:px-6 lg:px-8 py-6 sm:py-8">
            <!-- Branding -->
            <div class="text-center text-2xl font-cake">
                <span class="block leading-none">The Cake</span>
                <span class="text-4xl leading-none">Boutique</span>
            </div>

            <!-- Desktop Menu -->
            <div class="hidden lg:flex md:text-md md:space-x-6 uppercase font-corporate">
                <a href="#">Signature Cakes</a>
                <a href="#">Bespoke Cakes</a>
                <a href="#">Wedding Cakes</a>
                <a href="#">Cakesicles</a>
                <a href="#">Chocolates</a>
                <a href="#">Master Classes</a>
            </div>

            <!-- Right-side Icons -->
            <div class="hidden lg:flex items-center space-x-8">
                <!-- Search Icon -->
                <svg class="w-5 h-5 transition duration-150 ease-in-out cursor-pointer" fill="currentColor"
                    xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                    <path d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 
                    12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 
                    40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 
                    0S416 93.1 416 208zM208 352a144 144 0 1 0 
                    0-288 144 144 0 1 0 0 288z" />
                </svg>

                <!-- User Icon -->
                <svg class="w-5 h-5 transition duration-150 ease-in-out cursor-pointer" fill="currentColor"
                    xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                    <path d="M224 256A128 128 0 1 0 224 0a128 128 0 1 0 0 256zm-45.7 48C79.8 
                    304 0 383.8 0 482.3C0 498.7 13.3 512 29.7 
                    512l388.6 0c16.4 0 29.7-13.3 29.7-29.7C448 
                    383.8 368.2 304 269.7 304l-91.4 0z" />
                </svg>

                <!-- Shopping Cart Icon -->
                <svg class="w-5 h-5 transition duration-150 ease-in-out cursor-pointer" fill="currentColor"
                    xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
                    <path d="M0 24C0 10.7 10.7 0 24 0L69.5 0c22 0 41.5 12.8 50.6 32l411 0c26.3 
                0 45.5 25 38.6 50.4l-41 152.3c-8.5 31.4-37 53.3-69.5 53.3l-288.5 0 
                5.4 28.5c2.2 11.3 12.1 19.5 23.6 19.5L488 336c13.3 0 24 10.7 24 
                24s-10.7 24-24 24l-288.3 0c-34.6 0-64.3-24.6-70.7-58.5L77.4 
                54.5c-.7-3.8-4-6.5-7.9-6.5L24 48C10.7 48 0 37.3 0 24zM128 
                464a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm336-48a48 48 0 1 
                1 0 96 48 48 0 1 1 0-96z" />
                </svg>
            </div>

            <!-- Mobile Menu Button -->
            <button @click="isOpen = !isOpen" class="lg:hidden focus:outline-none relative w-8 h-8">
                <span class="block absolute h-0.5 w-8 bg-white transform transition duration-300 ease-in-out"
                    :class="isOpen ? 'rotate-45 top-3.5' : 'top-1'"></span>
                <span class="block absolute h-0.5 w-8 bg-white transition-all duration-300 ease-in-out"
                    :class="isOpen ? 'opacity-0' : 'top-3.5'"></span>
                <span class="block absolute h-0.5 w-8 bg-white transform transition duration-300 ease-in-out"
                    :class="isOpen ? '-rotate-45 top-3.5' : 'top-6'"></span>
            </button>
        </div>

        <!-- Mobile Menu -->
        <transition name="mobile-slide">
            <div v-if="isOpen"
                class="absolute top-full left-0 w-full z-40 flex flex-col justify-center space-y-10 py-16 bg-black bg-opacity-90 text-center text-sm uppercase font-corporate">
                <a href="#" @click="isOpen = false" class="hover:opacity-80 transition">Signature Cakes</a>
                <a href="#" @click="isOpen = false" class="hover:opacity-80 transition">Bespoke Cakes</a>
                <a href="#" @click="isOpen = false" class="hover:opacity-80 transition">Wedding Cakes</a>
                <a href="#" @click="isOpen = false" class="hover:opacity-80 transition">Cakesicles</a>
                <a href="#" @click="isOpen = false" class="hover:opacity-80 transition">Chocolates</a>
                <a href="#" @click="isOpen = false" class="hover:opacity-80 transition">Master Classes</a>
            </div>
        </transition>

    </nav>
</template>

<script>
export default {
    name: "Navbar",
    data() {
        return {
            isOpen: false,
            scrolled: false,
        };
    },
    mounted() {
        window.addEventListener("scroll", this.handleScroll);
    },
    beforeUnmount() {
        window.removeEventListener("scroll", this.handleScroll);
    },
    watch: {
        isOpen(newVal) {
            document.body.style.overflow = newVal ? "hidden" : "";
        },
    },
    methods: {
        handleScroll() {
            this.scrolled = window.scrollY > 10;
        },
    },
};
</script>

<style>
/* Mobile Menu Slide Animation */
.mobile-slide-enter-active,
.mobile-slide-leave-active {
    transition: all 0.3s ease;
}

.mobile-slide-enter-from {
    opacity: 0;
    transform: translateY(-10px);
}

.mobile-slide-enter-to {
    opacity: 1;
    transform: translateY(0);
}

.mobile-slide-leave-from {
    opacity: 1;
    transform: translateY(0);
}

.mobile-slide-leave-to {
    opacity: 0;
    transform: translateY(-10px);
}
</style>

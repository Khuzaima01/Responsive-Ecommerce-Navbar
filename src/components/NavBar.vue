<script setup>
import { ref } from "vue";

const isVisible = ref(false);

function toggleNav() {
  console.log("Before toggle:", isVisible.value);
  isVisible.value = !isVisible.value;
  console.log("After toggle:", isVisible.value);
}
</script>

<template>
  <div class="">
    <div class="bg-white border border-gray-300 p-3">
      <div class="container mx-auto grid lg:grid-cols-3 grid-cols-2 w-full">
        <div class="flex flex-col justify-center items-start">
          <p class="text-amber-600 text-xs md:text-sm">(+01) - 4890 - 3984</p>
          <p class="text-blue-800 text-xs md:text-sm">Our location</p>
        </div>
        <div class="lg:block hidden">
          <label
            for="default-search"
            class="mb-2 text-sm font-medium text-gray-900 sr-only"
            >Search</label
          >
          <div class="relative">
            <div
              class="absolute inset-y-0 start-0 flex items-center ps-3 pointer-events-none"
            >
              <svg
                class="w-4 h-4 text-amber-600"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 20 20"
              >
                <path
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"
                />
              </svg>
            </div>
            <input
              type="search"
              id="default-search"
              class="block w-full p-4 ps-10 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:border-2 focus:ring-amber-600 focus:border-amber-600 focus:outline-none"
              placeholder="Search..."
              required
            />
          </div>
        </div>
        <div class="flex items-center justify-end">
          <div class="flex items-center gap-3">
            <span class="text-amber-600 text-xs md:text-sm"> Login </span>
            <span>-</span>
            <span class="text-amber-600 text-xs md:text-sm"> Sign Up </span>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-amber-100 p-4">
      <div class="container mx-auto">
        <div class="grid grid-cols-3">
          <button
            @click="toggleNav"
            class="cursor-pointer md:hidden flex items-center"
          >
            <svg
              class="fill-amber-600 w-5 h-5 md:w-3 md:h-3"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 448 512"
            >
              <path
                d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"
              />
            </svg>
          </button>
          <div class="flex items-center md:justify-start justify-center">
            <h1 class="text-3xl font-bold text-amber-600 md:block hidden">
              Sentina.
            </h1>
          </div>
          <div
            class="flex items-center justify-center md:relative fixed md:bg-transparent bg-amber-100 md:h-auto h-screen md:left-auto left-[-100%] transition-left duration-300 ease-in-out"
            :class="{ 'left-[0%] w-[70%]': isVisible == true }"
          >
            <ul
              class="flex md:flex-row flex-col md:px-0 px-4 gap-5 whitespace-nowrap"
            >
              <li
                class="hover:bg-amber-300 cursor-pointer transition-all duration-300 ease-in-out"
              >
                Home
              </li>
              <li
                class="hover:bg-amber-300 cursor-pointer transition-all duration-300 ease-in-out"
              >
                Our Products
              </li>
              <li
                class="hover:bg-amber-300 cursor-pointer transition-all duration-300 ease-in-out"
              >
                About Us
              </li>
              <li
                class="hover:bg-amber-300 cursor-pointer transition-all duration-300 ease-in-out"
              >
                Contact Us
              </li>
            </ul>
          </div>
          <div class="flex items-center justify-end gap-4">
            <div class="cursor-pointer lg:hidden block">
              <svg
                class="fill-amber-600 md:w-5 md:h-5 w-4 h-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
              >
                <path
                  d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"
                />
              </svg>
            </div>
            <div class="relative cursor-pointer">
              <div
                class="absolute top-[-15px] right-[-10px] bg-red-500 text-white w-5 h-5 rounded-full flex items-center justify-center"
              >
                <span class="">1</span>
              </div>
              <svg
                class="fill-amber-600 md:w-5 md:h-5 w-4 h-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 576 512"
              >
                <path
                  d="M0 24C0 10.7 10.7 0 24 0H69.5c22 0 41.5 12.8 50.6 32h411c26.3 0 45.5 25 38.6 50.4l-41 152.3c-8.5 31.4-37 53.3-69.5 53.3H170.7l5.4 28.5c2.2 11.3 12.1 19.5 23.6 19.5H488c13.3 0 24 10.7 24 24s-10.7 24-24 24H199.7c-34.6 0-64.3-24.6-70.7-58.5L77.4 54.5c-.7-3.8-4-6.5-7.9-6.5H24C10.7 48 0 37.3 0 24zM128 464a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm336-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z"
                />
              </svg>
            </div>
            <div class="relative cursor-pointer">
              <div
                class="absolute top-[-15px] right-[-10px] bg-red-500 text-white w-5 h-5 rounded-full flex items-center justify-center"
              >
                <span class="">3</span>
              </div>
              <svg
                class="fill-amber-600 md:w-5 md:h-5 w-4 h-4"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
              >
                <path
                  d="M47.6 300.4L228.3 469.1c7.5 7 17.4 10.9 27.7 10.9s20.2-3.9 27.7-10.9L464.4 300.4c30.4-28.3 47.6-68 47.6-109.5v-5.8c0-69.9-50.5-129.5-119.4-141C347 36.5 300.6 51.4 268 84L256 96 244 84c-32.6-32.6-79-47.5-124.6-39.9C50.5 55.6 0 115.2 0 185.1v5.8c0 41.5 17.2 81.2 47.6 109.5z"
                />
              </svg>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

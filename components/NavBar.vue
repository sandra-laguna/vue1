<template>
  <nav class="bg-gray-800">
    <div class="mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <a href="/"><img class="h-8" src="~assets/img/amd-logo-white.svg" alt="logo" /></a>
        <div class="flex items-center">
          <div class="flex-shrink-0"></div>
          <div class="hidden md:block">
            <div class="ml-10 flex items-baseline">
              <a
                href="/"
                class="
                  px-3
                  py-2
                  rounded-md
                  font-medium
                  text-white
                  bg-gray-900
                  focus:outline-none
                  focus:text-white
                  focus:bg-gray-700
                "
                >Home</a
              >
              <a
                href="/nosotros"
                class="
                  ml-4
                  px-3
                  py-2
                  rounded-md
                  font-medium
                  text-gray-300
                  hover:text-white
                  hover:bg-gray-700
                  focus:outline-none
                  focus:text-white
                  focus:bg-gray-700
                "
                >Nosotros</a
              >
              <a
                href="/contacto"
                class="
                  ml-4
                  px-3
                  py-2
                  rounded-md
                  font-medium
                  text-gray-300
                  hover:text-white
                  hover:bg-gray-700
                  focus:outline-none
                  focus:text-white
                  focus:bg-gray-700
                "
                >Contacto</a
              >
            </div>
          </div>
        </div>

        <div class="-mr-2 flex md:hidden">
          <!-- Mobile menu button -->
          <button
            @click="toggle"
            class="
              inline-flex
              items-center
              justify-center
              p-2
              rounded-md
              text-gray-400
              hover:text-white
              hover:bg-gray-700
              focus:outline-none
              focus:bg-gray-700
              focus:text-white
            "
          >
            <svg
              :class="[isOpen ? 'hidden' : 'block', 'h-6 w-6']"
              stroke="currentColor"
              fill="none"
              viewBox="0 0 24 24"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
            </svg>
            <svg
              :class="[isOpen ? 'block' : 'hidden', 'h-6 w-6']"
              stroke="currentColor"
              fill="none"
              viewBox="0 0 24 24"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
            </svg>
          </button>
        </div>
      </div>
    </div>
    <div :class="[isOpen ? '' : 'hidden', 'md:hidden']">
      <div class="px-2 pt-2 pb-3 sm:px-3">
        <a
          href="/"
          class="
            block
            px-3
            py-2
            rounded-md
            text-base
            font-medium
            text-white
            bg-gray-900
            focus:outline-none
            focus:text-white
            focus:bg-gray-700
          "
          >Home</a
        >
        <a
          href="/nosotros"
          class="
            mt-1
            block
            px-3
            py-2
            rounded-md
            text-base
            font-medium
            text-gray-300
            hover:text-white
            hover:bg-gray-700
            focus:outline-none
            focus:text-white
            focus:bg-gray-700
          "
          >Nosotros</a
        >
        <a
          href="/contacto"
          class="
            mt-1
            block
            px-3
            py-2
            rounded-md
            text-base
            font-medium
            text-gray-300
            hover:text-white
            hover:bg-gray-700
            focus:outline-none
            focus:text-white
            focus:bg-gray-700
          "
          >Contacto</a
        >
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>

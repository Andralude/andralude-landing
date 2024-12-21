<template>
  <nav id="header" class="lg:fixed w-full z-30 top-0 text-white transition duration-300">
    <div class="w-full container mx-auto flex flex-wrap max-lg:flex-col items-center justify-between mt-0 py-2">
      <div class="pl-4 flex items-center">
        <a class="toggleColour text-white no-underline hover:no-underline font-bold" href="#">
          <img id="logo" class="h-12 inline" src="/assets/logo-white.svg" />
          <span class="ml-4 text-2xl lg:text-3xl align-middle">ANDRALUDE</span>
        </a>
      </div>
      <div
        class="flex items-center w-auto text-black z-20 max-lg:flex-col-reverse gap-2"
        id="nav-content">
        <ul class="flex flex-row justify-end flex-1 items-center">
          <!-- <li class="mr-3">
            <a class="inline-block py-2 px-4 text-black font-bold no-underline" href="#">Active</a>
          </li>
          <li class="mr-3">
            <a class="inline-block text-black no-underline hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#">link</a>
          </li> -->
          <li class="mr-3">
            <a class="inline-block text-white toggleColour underline py-2 px-4 max-lg:text-lg"
              href="https://train-annot.andralude.com">Train pour Annot</a>
          </li>
          <li class="mr-3">
            <a class="inline-block text-white toggleColour underline py-2 px-4 max-lg:text-lg"
              href="https://www.billetweb.fr/soiree-cine-folie">Ciné folie : Les bronzés</a>
          </li>
        </ul>
        <button id="navAction"
          class="lg:mx-0 hover:underline bg-white text-gray-800 font-bold rounded-2xl mt-4 lg:mt-0 py-2 px-4 mx-4 shadow opacity-75 focus:outline-none focus:shadow-outline transform transition hover:scale-105 duration-300 ease-in-out" href="#contact" :onClick="scrollToContact">
          Contact
        </button>
      </div>
    </div>
    <hr class="border-b border-gray-100 opacity-25 my-0 py-0" />
  </nav>
</template>

<script lang="ts">
export default {
  name: 'Header',
  mounted() {
    let scrollpos = window.scrollY;
    let header = document.getElementById("header");
    let logo = document.getElementById("logo") as HTMLImageElement;

    const applyScrolledClass = () => {
      if (window.innerWidth < 1024) {
        header!.classList.add("scrolled");
        logo!.src = "/assets/logo.svg";
      } else {
        if (scrollpos > 10) {
          header!.classList.add("scrolled");
          logo!.src = "/assets/logo.svg";
        } else {
          header!.classList.remove("scrolled");
          logo!.src = "/assets/logo-white.svg";
        }
      }
    };

    applyScrolledClass();

    window.addEventListener("resize", applyScrolledClass);

    document.addEventListener("scroll", function () {
      scrollpos = window.scrollY;
      applyScrolledClass();
    });
  },
  methods: {
    scrollToContact() {
      const contact = document.getElementById("contact");
      if (contact) {
        contact.scrollIntoView({ behavior: "smooth" });
      }
    }
  }
}
</script>

<style scoped>
.scrolled {
  background-color: white;
  box-shadow: 0 4px 2px -2px #bbbbbb90;
}

.scrolled #navAction {
  background-color: #d679a2;
  color: white;
}

.scrolled .toggleColour {
  color: rgb(98, 98, 98);
}
</style>
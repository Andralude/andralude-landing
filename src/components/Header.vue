<template>
  <nav id="header" class="fixed w-full z-30 top-0 text-white transition duration-300">
    <div class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 py-2">
      <div class="pl-4 flex items-center">
        <a class="toggleColour text-white no-underline hover:no-underline font-bold" href="#">
          <img id="logo" class="h-12 inline" src="/assets/logo-white.svg" />
          <span class="ml-2 text-2xl lg:text-3xl align-middle">ANDRALUDE</span>
        </a>
      </div>
      <div
        class="flex items-center w-auto text-black z-20"
        id="nav-content">
        <ul class="list-reset lg:flex justify-end flex-1 items-center">
          <!-- <li class="mr-3">
            <a class="inline-block py-2 px-4 text-black font-bold no-underline" href="#">Active</a>
          </li>
          <li class="mr-3">
            <a class="inline-block text-black no-underline hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#">link</a>
          </li> -->
          <li class="mr-3">
            <a class="inline-block text-black underline hover:text-gray-800 py-2 px-4"
              href="https://train-annot.spacegamers.fr/">Train pour Annot</a>
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
    let navcontent = document.getElementById("nav-content");
    let navaction = document.getElementById("navAction");
    let toToggle = document.querySelectorAll(".toggleColour");
    let logo = document.getElementById("logo") as HTMLImageElement;

    document.addEventListener("scroll", function () {
      /*Apply classes for slide in bar*/
      scrollpos = window.scrollY;

      if (scrollpos > 10) {
        header!.classList.add("bg-white");
        navaction!.classList.remove("bg-white");
        navaction!.classList.add("bg-[#d679a2]");
        navaction!.classList.remove("text-gray-800");
        navaction!.classList.add("text-white");
        //Use to switch toggleColour colours
        for (var i = 0; i < toToggle.length; i++) {
          toToggle[i].classList.add("text-gray-800");
          toToggle[i].classList.remove("text-white");
        }
        header!.classList.add("shadow");
        // change the src of logo
        logo!.src = "/assets/logo.svg";
      } else {
        header!.classList.remove("bg-white");
        navaction!.classList.remove("bg-[#d679a2]");
        navaction!.classList.add("bg-white");
        navaction!.classList.remove("text-white");
        navaction!.classList.add("text-gray-800");
        //Use to switch toggleColour colours
        for (var i = 0; i < toToggle.length; i++) {
          toToggle[i].classList.add("text-white");
          toToggle[i].classList.remove("text-gray-800");
        }
        header!.classList.remove("shadow");
        logo!.src = "/assets/logo-white.svg";
      }
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
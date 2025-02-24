<script>
  import { onMount } from 'svelte';
  import '../app.css'
  export let year = new Date().getFullYear();
  import facebook from '../image/facebook1.png'
  import twitter from '../image/twit.png'
  import linkdin from '../image/linkedIn.png'
  
  let isMobileMenuOpen = false;
  
  function toggleMenu() {
    isMobileMenuOpen = !isMobileMenuOpen;
  }

 
  function closeMenuOnClickOutside(e) {
    const menu = document.getElementById('mobile-menu');
    const button = document.getElementById('menu-button');

   
    if (menu && button) {
      if (!button.contains(e.target) && !menu.contains(e.target)) {
        isMobileMenuOpen = false;
      }
    }
  }

  
  onMount(() => {
    document.addEventListener('click', closeMenuOnClickOutside);

    return () => {
      document.removeEventListener('click', closeMenuOnClickOutside);
    };
  });
</script>

<nav class="bg-gray-800 text-white p-4">
  <div class="container mx-auto flex justify-between items-center">
    <a href="/" class="text-xl font-bold">World Tech Expo</a>
  
    <!-- Hamburger Menu Button for Mobile -->
    <button
      id="menu-button"
      class="md:hidden focus:outline-none"
      on:click={toggleMenu}
    >
      ☰
    </button>

    <!-- Desktop Menu -->

    <div class="hidden md:flex space-x-4">
      <a href="/speakers" >Speakers</a>
      <a href="/schedule" >Schedule</a>
      <a href="/sponsors" >Sponsors</a>
      <a href="/about">About</a>
      <a href="/contact" >Contact</a>
    </div>
  </div>

  <!-- Mobile Menu -->
  <div id="mobile-menu" class="md:hidden mt-4" class:hidden={!isMobileMenuOpen}>
    <a href="/speakers" class="block py-2 hover:underline">Speakers</a>
    <a href="/schedule" class="block py-2 hover:underline">Schedule</a>
    <a href="/sponsors" class="block py-2 hover:underline">Sponsors</a>
    <a href="/about" class="block py-2 hover:underline">About</a>
    <a href="/contact" class="block py-2 hover:underline">Contact</a>
  </div>
</nav>

<slot />



<footer class="bg-[#0a0b29] text-white py-12">
  <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-4 gap-8">
    
    <!-- Logo & Description -->
    <div>
      <img src="https://i0.wp.com/tmtel.com/wp-content/uploads/2020/02/a0cd1c6667633054256d9a1d09dbba59.jpg?resize=1200%2C867&ssl=1" alt="World AI Tech Expo" class="h-14 mb-4" />
      <p class="text-gray-300 text-sm">
        The World AI Technology Expo in India stands as the largest and most comprehensive AI exhibition and seminar globally, offering an unparalleled platform for innovation and collaboration.
      </p>
      <div class="flex space-x-4 mt-4">
       <img src={linkdin} alt="" class="w-8 h-8 ring-2 shadow-lg transition-all duration-700 hover:scale-130">
       <img src={twitter} alt="" class="w-8 h-8 shadow-lg ring-2 transition-all duration-700 hover:scale-130 ">
       <img src={facebook} alt="" class="w-8 h-8 ring-2 shadow-lg transition-all duration-700 hover:scale-130 ">

      </div>
    </div>

    <!-- Useful Links -->
    <div>
      <h3 class="text-lg font-bold text-cyan-400">Useful Links</h3>
      <ul class="mt-3 space-y-2 text-sm">
        <li><a href="/home" class="hover:text-cyan-300">› Home</a></li>
        <li><a href="/speakers" class="hover:text-cyan-300">› Speakers</a></li>
        <li><a href="/event" class="hover:text-cyan-300">› Event Details</a></li>
        <li><a href="/exhibit" class="hover:text-cyan-300">› Exhibit</a></li>
        <li><a href="/sponsor" class="hover:text-cyan-300">› Become a Sponsor</a></li>
      </ul>
    </div>

    <!-- AI & Conferences -->
    <div>
      <h3 class="text-lg font-bold text-cyan-400">AI & Conferences</h3>
      <ul class="mt-3 space-y-2 text-sm">
        <li>› AI Speaker Sessions</li>
        <li>› AI Seminars</li>
        <li>› AI Hackathon</li>
        <li>› AI Expo</li>
        <li>› AI Conference</li>
      </ul>
    </div>

    <!-- Contact Section -->
    <div>
      <h3 class="text-lg font-bold text-cyan-400">Contact Us</h3>
      <p class="mt-3 text-sm text-gray-300 flex items-center">
        <i class="fas fa-phone-alt text-cyan-400 mr-2"></i> +971 5858 7 2014
      </p>
      <p class="mt-1 text-sm text-gray-300 flex items-center">
        <i class="fas fa-envelope text-cyan-400 mr-2"></i> events@goldentreeevent.com
      </p>
    </div>

  </div>

  <!-- Copyright -->
  <div class="mt-10 border-t border-gray-600 text-center pt-4 text-gray-400 text-sm">
    © {year} World AI Technology Expo. All rights reserved.
  </div>
</footer>


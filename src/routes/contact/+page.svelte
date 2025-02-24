<script>
  import fa from '../../image/facebook1.png'
  import linkdin from '../../image/linkdin.png'
  import twitter from '../../image/twitte.png'
</script>

<div class="min-h-screen bg-gradient-to-b from-blue-900 to-teal-600 p-5">
  <div class="container mx-auto">
    <h1 class="text-3xl font-bold text-center mb-8 text-white">Contact Us</h1>
    <form class="bg-white p-6 rounded-lg shadow-lg max-w-md mx-auto">
      <div class="mb-4">
        <label for="name" class="block text-gray-700">Name</label>
        <input type="text" id="name" class="w-full px-4 py-2 border rounded-lg" />
      </div>
      <div class="mb-4">
        <label for="email" class="block text-gray-700">Email</label>
        <input type="email" id="email" class="w-full px-4 py-2 border rounded-lg" />
      </div>
      <div class="mb-4">
        <label for="message" class="block text-gray-700">Message</label>
        <textarea id="message" class="w-full px-4 py-2 border rounded-lg"></textarea>
      </div>
      <button type="submit" class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700 transition">
        Send Message
      </button>
    </form>

    <!-- Social Media Links -->
    <div class="mt-8 text-center ">
      <h2 class="text-xl font-semibold text-white mb-4">Follow Us</h2>
      <div class="flex justify-center space-x-4 ">
       <img src={fa} alt="facebook" class="w-8 h-8 shadow-lg transition-all duration-700 hover:scale-130">
       <img src={linkdin} alt="linkdin" class="w-8 h-8 shadow-lg transition-all duration-700 hover:scale-130">
       <img src={twitter} alt="twitter" class="w-8 h-8 shadow-lg transition-all duration-700 hover:scale-130">
      </div>
    </div>
  </div>
</div>
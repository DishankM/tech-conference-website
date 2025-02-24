<script>
  const conference = {
    name: "Tech Innovators Conference 2025",
    description: "The Tech Innovators Conference brings together industry leaders, pioneers, and enthusiasts to explore the future of technology. With insightful keynotes, engaging panels, and interactive workshops, this conference is the perfect place to gain knowledge and connect with like-minded professionals. Join us as we dive deep into the latest trends in artificial intelligence, robotics, blockchain, and more.",
    date: "February 24-26, 2025",
    location: "San Francisco, CA",
    website: "https://www.techinnovators.com",
  };
</script>

<div class="min-h-screen bg-gradient-to-b from-blue-900 to-teal-600 py-12">
  <div class="container mx-auto px-6">
    
    <div class="text-center mb-16">
      <h1 class="text-5xl font-extrabold text-white mb-4">About {conference.name}</h1>
      <p class="text-xl text-gray-300">An immersive experience into the world of technology and innovation.</p>
    </div>

    <!-- About Section -->
    <div class="bg-white p-8 rounded-lg shadow-xl bg-opacity-90">
      <p class="text-lg text-gray-800 leading-relaxed mb-6">
        {conference.description}
      </p>

      <div class="mt-6">
        <p class="text-xl font-semibold text-teal-500">Date:</p>
        <p class="text-lg text-gray-700">{conference.date}</p>
      </div>

      <div class="mt-4">
        <p class="text-xl font-semibold text-teal-500">Location:</p>
        <p class="text-lg text-gray-700">{conference.location}</p>
      </div>

      <div class="mt-6">
        <a
          href={conference.website}
          target="_blank"
          rel="noopener noreferrer"
          class="inline-block bg-teal-500 text-white py-2 px-6 rounded-lg text-lg font-semibold hover:bg-teal-600 transition duration-300"
        >
          Visit Website
        </a>
      </div>
    </div>
  </div>
</div>

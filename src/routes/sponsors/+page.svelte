<script>
 
  
  const tagline = "Meet Tech Experts from Startups to Fortune 500 Companies";
  
  const speakers = [
    {
      name: "Nitin Akarte",
      title: "CTO at TechCorp",
      image: "https://www.apetogentleman.com/wp-content/uploads/2018/06/male-models-marlon.jpg",
      bio: "Expert in AI networking, supercomputer deployments, and cybersecurity...",
      company: "Microsoft"
    },
    {
      name: "James Hunter",
      title: "Lead Developer at DevWorks",
      image: "https://www.apetogentleman.com/wp-content/uploads/2018/06/male-models-marlon.jpg",
      bio: "Specialist in full-stack development and AI-driven applications...",
      company: "Google"
    }
  ];

  const sponsors = {
    Gold: [
      { name: "OpenAI", logo: "https://th.bing.com/th/id/OIP.Adw37M6qHPVuGYVWDuJkkQAAAA?rs=1&pid=ImgDetMain", link: "https://www.chatgpt.com" },
      { name: "Google", logo: "https://th.bing.com/th/id/OIP.2cc8ZdhHcP-ga1CHADKaYQHaEK?w=2048&h=1152&rs=1&pid=ImgDetMain", link: "https://www.google.com" }
    ],
    Silver: [
      { name: "Microsoft", logo: "https://logos-world.net/wp-content/uploads/2020/09/Microsoft-Logo-2012-present.jpg", link: "https://www.microsoft.com" },
      { name: "TCS", logo: "https://camunda.com/wp-content/uploads/2022/09/TCS_NewLogo_Final_RGB.png", link: "https://www.tcs.com" }
    ],
    Bronze: [
      { name: "Wipro", logo: "https://th.bing.com/th/id/OIP.kNtVVyILqQkxHBffbCqkyQHaEK?rs=1&pid=ImgDetMain", link: "https://www.wipro.com" },
      { name: "HP", logo: "https://th.bing.com/th/id/OIP.udBtzCWKRQuRttMV_wkbrgHaEK?rs=1&pid=ImgDetMain", link: "https://www.hp.com" },
      { name: "IBM", logo: "https://th.bing.com/th/id/OIP.wD_fKi6K-okPUivWxldiggHaEK?rs=1&pid=ImgDetMain", link: "https://www.IBM.com" },
      { name: "Accenture", logo: "https://logosmarcas.net/wp-content/uploads/2020/06/Accenture-Logo.png", link: "https://www.accenture.com" }
    ]
  };
</script>

<div class="min-h-screen bg-gray-100">
  <!-- Hero Section -->
  <section class="bg-cover bg-center text-white py-20 px-6" style="background-image: url('https://png.pngtree.com/thumb_back/fh260/background/20200714/pngtree-modern-double-color-futuristic-neon-background-image_351866.jpg');">
    <div class="max-w-2xl mx-auto text-center">
      <h1 class="text-5xl font-bold mb-4">The One & Only <span class="text-yellow-300">CORPORATE</span> Focused Tech Conference</h1>
      <p class="text-xl italic mb-8">{tagline}</p>
     
      <button class="bg-yellow-300 text-blue-600 px-6 py-3 rounded-md font-semibold hover:bg-yellow-400 transition">
        Register Now
      </button>
    </div>
  </section>

  <!-- Sponsors Section -->
  <section class="min-h-screen bg-gradient-to-b from-blue-900 to-teal-600 py-16 px-6">
    <div class="max-w-6xl mx-auto text-center">
      <h2 class="text-4xl font-bold text-cyan-300">Our Supporting Sponsors</h2>
      <p class="text-gray-300 mt-2">We are grateful for the amazing support from these incredible brands.</p>
    </div>
    {#each Object.entries(sponsors) as [tier, tierSponsors]}
      <div class="mt-10">
        <h3 class="text-2xl text-yellow-300 font-bold text-center mb-4">{tier} Sponsors</h3>
        <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-10 max-w-5xl mx-auto">
          {#each tierSponsors as sponsor}
            <div class="flex justify-center items-center p-6 bg-white rounded-lg shadow-xl transform transition duration-500 hover:scale-105 hover:shadow-2xl">
              <a href={sponsor.link} target="_blank" rel="noopener noreferrer">
                <img src={sponsor.logo} alt={sponsor.name} class="h-24 md:h-32 object-contain transition-all duration-300 transform hover:scale-110" />
              </a>
            </div>
          {/each}
        </div>
      </div>
    {/each}
  </section>
</div>

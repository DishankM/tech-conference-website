<script>

  import { onMount } from 'svelte';
  let days, hours, minutes, seconds;

  const eventDate = new Date('2025-03-15T09:00:00').getTime();

  function updateCountdown() {
      const now = new Date().getTime();
      const timeLeft = eventDate - now;

      days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
      hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
      seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
  }

  onMount(() => {
      updateCountdown();
      const timer = setInterval(updateCountdown, 1000);
      return () => clearInterval(timer);
  });

  const tagline = "MEET TECH EXPERTS FROM STARTUPS TO FORTUNE 500 COMPANIES";
  const speakers = [
      {
          name: "Nitin Akarte",
          title: "CTO at TechCorp",
          image: "https://www.apetogentleman.com/wp-content/uploads/2018/06/male-models-marlon.jpg",
          bio: "Visionary leader in AI networking, supercomputer deployments, and cybersecurity...",
          company: "Microsoft",
      },
      {
          name: "James Hunter",
          title: "Lead Developer at DevWorks",
          image: "https://www.apetogentleman.com/wp-content/uploads/2018/06/male-models-marlon.jpg",
          bio: "Expert in AI networking, supercomputer deployments, and cybersecurity...",
          company: "Google",
      },
      {
      name: "Aniket Patil",
      title: "Head of Engineering, R&D Services, and Digital Services for HCL Tech",
      image: "https://th.bing.com/th/id/OIP.YIre5HGHiqBa7DCmrF4KwwHaJQ?rs=1&pid=ImgDetMain", 
      bio: "Aniket Patil is the Head of Engineering, R&D Services, and Digital Services for HCL Tech in the Middle East, based in Dubai. A visionary leader in digital transformation and AI,",
      company: "HCL",
    },
    {
      name: "Padmapriya Mohankumar",
      title: "Senior Engineering Manager - Machine Learning - PayPal",
      image: "https://college.georgetown.edu/wp-content/uploads/2021/05/20150401-Faculty_0347-1-edited-1154x1536.jpg", 
      bio: "Padmapriya Mohankumar is an accomplished AI researcher, speaker, and innovator with multiple patents and research publications in emerging technologies, cybersecurity, and financial AI. ",
      company: "Paypal",
    },
  ];
</script>

<style>
  
  .speaker-card:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 16px rgba(255, 255, 255, 0.2);
  }
  .parallax {
      background-attachment: fixed;
      background-size: cover;
  }
</style>

<div class="min-h-screen bg-gray-100">
  <!-- Hero Section with Parallax Effect -->
  <section class="parallax bg-[url(https://png.pngtree.com/thumb_back/fh260/background/20200714/pngtree-modern-double-color-futuristic-neon-background-image_351866.jpg)] text-white py-25">
      <div class="container mx-auto max-w-[900px] text-start">
          <h1 class="lg:text-5xl md:text-3xl font-bold mb-4">The One & Only <span class="text-yellow-300">CORPORATE</span> focused TECH Conference in the World</h1>
          <p class="lg:text-xl md:text-[16px] p-2 mb-8 italic">{tagline}</p>
          <div class="bg-gray-500 text-yellow-300 text-2xl font-bold p-4 rounded-lg inline-block mt-7 mr-6 countdown">
              Event starts in: <span>{days}</span>d <span>{hours}</span>h <span>{minutes}</span>m <span>{seconds}</span>s
          </div>
          <button class="bg-yellow-300 text-blue-600 px-8 py-4 rounded-md font-semibold hover:bg-blue-100 transition lg:mt-1 mt-6">
              <a href="/contact">Register Now</a>
          </button>
      </div>
  </section>

  <!-- Featured Speakers Section -->
  <div class="min-h-screen bg-gradient-to-b from-blue-900 to-teal-700 py-12">
      <div class="max-w-6xl mx-auto text-center">
          <h1 class="text-4xl font-bold text-cyan-300">Meet The Speakers of Upcoming Sessions</h1>
          <p class="text-gray-300 mt-2">50+ speakers from the world's top AI companies.</p>
      </div>

      <div class="mt-10 grid grid-cols-1 md:grid-cols-2 gap-10 max-w-5xl mx-auto p-5">
          {#each speakers as speaker}
              <div class="speaker-card flex bg-gradient-to-r from-cyan-800 to-teal-700 text-white rounded-lg shadow-lg overflow-hidden transition-transform duration-300">
                  <img src={speaker.image} alt={speaker.name} class="w-50 h-40% object-cover rounded-l-lg overflow-auto" />
                  <div class="p-6 flex flex-col justify-between w-full">
                      <div>
                          <h3 class="lg:text-lg text-sm font-bold text-cyan-200">{speaker.name}</h3>
                          <p class="text-yellow-400 font-semibold lg:text-lg text-sm">{speaker.title}</p>
                          <p class="lg:text-sm text-[10px] mt-2">{speaker.bio}</p>
                      </div>
                      <div class="text-right">
                          <span class="bg-yellow-400 text-black text-xs px-3 py-1 rounded-full">{speaker.company}</span>
                      </div>
                  </div>
              </div>
          {/each}
      </div>
  </div>
</div>

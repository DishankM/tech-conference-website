<script>
  const schedule = [
    {
      image: "https://th.bing.com/th/id/OIP.YIre5HGHiqBa7DCmrF4KwwHaJQ?rs=1&pid=ImgDetMain",
      date: "2025-02-24",
      time: "10:00 AM",
      topic: "Opening Keynote",
      speaker: "Jane Doe",
      details: "The Opening Keynote is typically the first major session of the event and sets the tone for the entire conference. It is often delivered by a distinguished speaker, such as a high-profile industry leader or visionary, who introduces the theme or purpose of the event. During the keynote, the speaker will usually provide insights on important trends, challenges, or innovations within the industry and inspire the audience for the sessions to come. The Opening Keynote often highlights the event’s goals, mission, and key messages, ensuring that attendees are excited and motivated for the rest of the conference"
      
    },
    {
      image: "https://www.apetogentleman.com/wp-content/uploads/2018/06/male-models-marlon.jpg",
      date: "2025-02-24",
      time: "11:00 AM",
      topic: "Future of AI",
      speaker: "John Smith",
      details:"The 'Future of AI' session explores the cutting-edge advancements and potential of artificial intelligence in shaping industries and society. Experts in the field will discuss the latest developments in AI technologies, including machine learning, deep learning, and natural language processing, and their applications across sectors such as healthcare, finance, automation, and more. The session will address key challenges such as ethics, data privacy, and the impact of AI on jobs, as well as explore the future implications of AI in transforming how we live and work. "
      
    },
  ];
</script>

<div class="min-h-screen bg-gradient-to-b from-blue-900 to-teal-600 py-12">
  <div class="container mx-auto px-6">
    
    <div class="text-center mb-12">
      <h1 class="text-4xl font-bold text-white">Conference Schedule</h1>
      <p class="text-lg text-gray-200">Stay updated on all sessions throughout the event</p>
    </div>

  
    <div class="space-y-8 lg:w-6xl ">
      {#each schedule as session}
        <div class=" bg-opacity-80 bg-gray-500 p-6 rounded-lg  border-b border-gray-600 shadow-lg transition-all duration-700 hover:scale-110">
          <div class="flex flex-col md:flex-row items-center">
            <img src={session.image} alt={session.speaker} class="w-45 h-65 object-cover rounded-md overflow-hidden"/>

            <p class="max-w-180 ml-10 mt-10 text-amber-50">{session.details}</p>
          </div>
          
          <p class="text-sm text-gray-300">{session.date} | {session.time}</p>
          <h3 class="text-2xl font-semibold text-yellow-400 mt-2">{session.topic}</h3>
          <p class="text-lg text-gray-100 mt-1 italic ">{session.speaker}</p>
        </div>
      {/each}
    </div>
  </div>
</div>

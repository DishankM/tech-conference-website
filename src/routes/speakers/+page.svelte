<script>
  const speakers = [
    {
      name: "Nitin Akarte",
      title: "AI Network Director - Microsoft Inc",
      image: "https://www.apetogentleman.com/wp-content/uploads/2018/06/male-models-marlon.jpg", 
      bio: "Nitin Akarte is a visionary leader and expert in AI networking, supercomputer deployments, and cybersecurity...",
      company: "Microsoft",
    },
    {
      name: "James Hunter",
      title: "Program Director @ IBM | Driving DevOps Automation and AI",
      image: "https://th.bing.com/th/id/OIP.UvVU9RQtcmWUTyIAB7pPGAHaLD?rs=1&pid=ImgDetMain", 
      bio: "James Hunter is the Program Director for DevOps at IBM, driving automation and generative AI...",
      company: "IBM",
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
    {
      name: "Manish Vaidaya",
      title: "Data Science & Analytics Head | Business Intelligence - Department of Culture and Tourism",
      image: "https://images.unsplash.com/photo-1592009309602-1dde752490ae?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&w=1000&q=80", 
      bio: "A results-driven leader in Data Science and Analytics, passionate about leveraging AI and data to drive innovation, optimize operations, and deliver actionable insights. With 15+ years of experience in AI ML, and data-driven strategy, I blend technical",
      company: "DCT",
    },
    {
      name: "Alizabeth Pearson",
      title: "Director & PMO for Oscar (Artificial Intelligence) at AECOM",
      image: "https://res.cloudinary.com/dpmykpsih/image/upload/c_fill,f_auto,q_90,w_800/iredell-health-system-site-359/media/1509005cae7746ab8cfff9fcd917b392/rachel-disanto-md-ipn.jpg", 
      bio: "Alizabeth Pearson is a global transformation leader with expertise in marketing, communications, and project management, currently serving as Director & PMO for Oscar (Artificial Intelligence) at AECOM.",
      company: "AECOM",
    },
  ];
</script>
<style>
  
  
</style>

<div class="min-h-screen bg-gradient-to-b from-blue-900 to-teal-700 py-12">
  <div class="max-w-6xl mx-auto text-center">
    <h1 class="text-4xl font-bold text-cyan-300">Few of Our Speakers</h1>
    <p class="text-gray-300 mt-2">50+ speakers from the world's top AI companies.</p>
  </div>

  <div class="mt-5 grid grid-cols-1 md:grid-cols-2 gap-20 max-w-7xl mx-auto p-5 space-evenly">
    {#each speakers as speaker}
      <div class=" flex flex-col sm:flex-row bg-gradient-to-r from-cyan-800 to-teal-700 text-white 
      shadow-lg transition-all duration-700 hover:scale-90">
        
        <div class="sm:w-1/3 ">
          <img src={speaker.image} alt={speaker.name} class="lg:w-[180px] h-100% object-cover rounded-t-lg sm:rounded-l-lg w-full h-full" />
        </div>
  
        <div class=" p-6 flex flex-col justify-between w-full">
          <div >
            <h3 class="lg:text-lg text-sm font-bold text-cyan-200">{speaker.name}</h3>
            <p class="text-yellow-400 font-semibold lg:text-lg text-sm">{speaker.title}</p>
            <p class="lg:text-sm text-[10px] mt-2">{speaker.bio} <a href="#" class="text-blue-300 underline">read more...</a></p>
          </div>
          <div class="text-right">
            <span class="bg-yellow-400 text-black text-xs px-3 py-1 rounded-full">{speaker.company}</span>
          </div>
        </div>
      </div>
    {/each}
  </div>
</div>

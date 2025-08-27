<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>S D R S</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    html { scroll-behavior: smooth; }

    /* Package cards */
    .active-package {
      border: 2px solid #2563eb;
      box-shadow: 0 0 15px rgba(37, 99, 235, 0.5);
      transform: scale(1.02);
      transition: all 0.3s ease;
    }
    .package-card {
      transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
    }
    .package-card:hover {
      transform: scale(1.03);
      box-shadow: 0 15px 25px rgba(0,0,0,0.2);
      border-color: #2563eb;
    }

    /* Buttons hover */
    .btn-hover {
      transition: transform 0.3s ease, box-shadow 0.3s ease, background-color 0.3s ease;
    }
    .btn-hover:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 20px rgba(0,0,0,0.3);
    }

    /* Hero blobs */
    .animate-pulse-slow {
      animation: pulse 6s ease-in-out infinite;
    }
    @keyframes pulse {
      0%,100% { transform: scale(1); opacity: 0.2; }
      50% { transform: scale(1.2); opacity: 0.3; }
    }

    /* Promo video effect */
    #promo {
      position: relative;
      overflow: hidden;
      height: 500px;
    }
    .promo-slide {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      opacity: 0;
      transition: opacity 1s ease-in-out;
    }
    .promo-slide.active {
      opacity: 1;
    }
    .promo-overlay {
      position: absolute;
      top: 0;
      left:0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.4);
    }
    .promo-content {
      position: relative;
      z-index: 10;
    }
  </style>
</head>
<body class="font-sans text-gray-900">

  <!-- Navigation -->
  <header class="sticky top-0 bg-white shadow z-50">
    <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
      <div class="text-2xl font-bold text-blue-600">S D R S</div>
      <nav class="space-x-6">
        <a href="#about" class="text-gray-700 hover:text-blue-600 font-medium">About</a>
        <a href="#pricing" class="text-gray-700 hover:text-blue-600 font-medium">Packages</a>
        <a href="#contact" class="text-gray-700 hover:text-blue-600 font-medium">Contact</a>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <section class="relative bg-gradient-to-r from-blue-600 via-indigo-600 to-purple-600 text-white py-28 px-6 text-center overflow-hidden">
    <div class="max-w-4xl mx-auto relative z-10">
      <h1 class="text-4xl md:text-6xl font-extrabold mb-4">Welcome to Steph’s Drone & Revamping Services</h1>
      <p class="mt-4 text-lg md:text-2xl text-gray-100 leading-relaxed">
        Your dedicated team for breathtaking aerial photography, professional property revamps, and creative visual storytelling.  
        We capture the essence of every space and event, making your listings and memories truly unforgettable.
      </p>
      <a href="#pricing" class="mt-8 inline-block px-8 py-4 bg-white text-blue-600 font-semibold rounded-xl shadow-lg btn-hover hover:bg-gray-100">
        Explore Our Packages
      </a>
    </div>
    <div class="absolute inset-0 -z-10">
      <img src="https://images.unsplash.com/photo-1600585154340-be6161f1b54d?auto=format&fit=crop&w=1600&q=80" alt="Drone aerial view" class="w-full h-full object-cover opacity-30">
      <div class="absolute w-96 h-96 bg-indigo-500 opacity-20 rounded-full top-10 left-10 animate-pulse-slow"></div>
      <div class="absolute w-72 h-72 bg-purple-500 opacity-15 rounded-full bottom-0 right-16 animate-pulse-slow"></div>
    </div>
  </section>

  <!-- Promo Video-Like Section -->
  <section id="promo">
    <!-- Slides -->
    <img src="https://images.unsplash.com/photo-1568605114967-8130f3a36994?auto=format&fit=crop&w=1600&q=80" class="promo-slide active" alt="Jamaican property 1">
    <img src="https://images.unsplash.com/photo-1505691723518-41cb3c27f8aa?auto=format&fit=crop&w=1600&q=80" class="promo-slide" alt="Jamaican property 2">
    <img src="https://images.unsplash.com/photo-1505691938895-1758d7feb511?auto=format&fit=crop&w=1600&q=80" class="promo-slide" alt="Jamaican property 3">
    
    <!-- Overlay -->
    <div class="promo-overlay"></div>
    
    <!-- Content -->
    <div class="promo-content flex flex-col items-center justify-center text-center text-white h-full px-6">
      <img src="https://YOUR_LOGO_URL_HERE.png" alt="SDRS Logo" class="w-48 mb-4">
      <h2 class="text-4xl md:text-5xl font-extrabold mb-4">Experience Your Property Like Never Before</h2>
      <p class="text-lg md:text-2xl mb-6">
        Stunning aerial shots, polished interiors, and professional property styling.<br>
        Showcase your Jamaican property and attract buyers or renters instantly.
      </p>
      <a href="#contact" class="inline-block px-8 py-4 bg-blue-600 hover:bg-blue-700 text-white font-semibold rounded-xl shadow-lg btn-hover">
        Book Your Package Today
      </a>
      <div class="mt-6 text-gray-200 text-sm md:text-base">
        📧 <a href="mailto:Stephsdronerevampingservices@gmail.com" class="underline hover:text-white">Stephsdronerevampingservices@gmail.com</a><br>
        📸 Instagram: <a href="https://instagram.com/Stephsdronerevampingservices" class="underline hover:text-white">@Stephsdronerevampingservices</a>
      </div>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="py-20 px-6 bg-white">
    <div class="max-w-5xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold mb-6">About Us</h2>
      <p class="text-lg text-gray-700 leading-relaxed">
        Turn Your Property into a Showstopper with Steph’s Drone & Revamping Services...
      </p>
    </div>
  </section>

  <!-- Packages -->
  <section id="pricing" class="py-20 px-6 bg-gray-50">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-12">Packages</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <!-- Package cards unchanged -->
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-20 px-6 bg-white">
    <div class="max-w-3xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-8">Get in Touch</h2>
      <form action="https://formsubmit.co/stephsdronerevampingservices@gmail.com" method="POST" class="space-y-6 bg-gray-50 p-8 rounded-2xl shadow">
        <!-- Contact form unchanged -->
      </form>
    </div>
  </section>

  <script>
    // Promo slide rotation
    const slides = document.querySelectorAll('.promo-slide');
    let currentSlide = 0;
    setInterval(() => {
      slides[currentSlide].classList.remove('active');
      currentSlide = (currentSlide + 1) % slides.length;
      slides[currentSlide].classList.add('active');
    }, 5000); // Change slide every 5 seconds

    // Package selection script
    const packageCards = document.querySelectorAll(".package-card");
    const packageInput = document.querySelector("#selectedPackage");
    const interestDropdown = document.querySelector("#interest");

    packageCards.forEach(card => {
      card.addEventListener("click", () => {
        packageCards.forEach(c => c.classList.remove("active-package"));
        card.classList.add("active-package");
        const selected = card.dataset.package;
        packageInput.value = selected;
        interestDropdown.value = selected;
      });
    });

    document.querySelectorAll(".book-btn").forEach(btn => {
      btn.addEventListener("click", () => {
        const selected = btn.dataset.package;
        packageInput.value = selected;
        interestDropdown.value = selected;
        packageCards.forEach(c => {
          c.classList.toggle("active-package", c.dataset.package === selected);
        });
        document.querySelector("#contact").scrollIntoView({ behavior: "smooth" });
      });
    });
  </script>

</body>
</html>

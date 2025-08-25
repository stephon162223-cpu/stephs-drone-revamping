<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Steph’s Drone & Revamping Services</title>
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

    /* Portfolio hover */
    .portfolio-img:hover {
      transform: scale(1.05);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      box-shadow: 0 10px 20px rgba(0,0,0,0.3);
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
  </style>
</head>
<body class="font-sans text-gray-900">

  <!-- Navigation -->
  <header class="sticky top-0 bg-white shadow z-50">
    <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
      <div class="text-2xl font-bold text-blue-600">Steph’s Drone</div>
      <nav class="space-x-6">
        <a href="#about" class="text-gray-700 hover:text-blue-600 font-medium">About</a>
        <a href="#portfolio" class="text-gray-700 hover:text-blue-600 font-medium">Portfolio</a>
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
      <div class="absolute w-96 h-96 bg-indigo-500 opacity-20 rounded-full top-10 left-10 animate-pulse-slow"></div>
      <div class="absolute w-72 h-72 bg-purple-500 opacity-15 rounded-full bottom-0 right-16 animate-pulse-slow"></div>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="py-20 px-6 bg-white">
    <div class="max-w-5xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold mb-6">About Us</h2>
      <p class="text-lg text-gray-700 leading-relaxed">
        We specialize in drone photography and videography, capturing breathtaking aerial shots that highlight the unique features of every property. From real estate listings and Airbnb rentals to private estates and commercial spaces, we also create polished interior and exterior photography to showcase your space from every angle. Beyond imagery, our property revamping service adds modern styling and creative staging to elevate appeal and performance. Whether you’re marketing a home for sale, boosting Airbnb bookings, or promoting an event, our team brings your vision to life with professionalism, creativity, and excellence.
      </p>
    </div>
  </section>

  <!-- Portfolio -->
  <section id="portfolio" class="py-20 px-6 bg-gray-50">
    <div class="max-w-7xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold mb-12">Portfolio</h2>
      <div class="grid md:grid-cols-3 gap-6">
        <img src="https://images.unsplash.com/photo-1560185127-6fcb9f5bdebe?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Luxury villa Jamaica">
        <img src="https://images.unsplash.com/photo-1599423300746-b62533397364?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Drone aerial property Jamaica">
        <img src="https://images.unsplash.com/photo-1580584124513-cb417a5b0a43?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Landscape Jamaica">
      </div>
    </div>
  </section>

  <!-- Packages -->
  <!-- (unchanged – all 5 packages included) -->

  <!-- Contact -->
  <!-- (unchanged – sends email via formsubmit) -->

  <script>
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

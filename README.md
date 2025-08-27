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

    /* Video overlay text */
    .video-overlay {
      background: rgba(0, 0, 0, 0.3);
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

  <!-- Promo Video Section -->
  <section id="promo" class="relative w-full h-[500px] overflow-hidden">
    <video class="w-full h-full object-cover" autoplay muted loop playsinline>
      <source src="https://YOUR_VIDEO_URL_HERE.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div class="absolute inset-0 video-overlay"></div>
    <div class="absolute inset-0 flex flex-col justify-center items-center text-center text-white px-6">
      <img src="https://YOUR_LOGO_URL_HERE.png" alt="SDRS Logo" class="w-36 mb-4">
      <h2 class="text-3xl md:text-5xl font-extrabold mb-2">Experience Your Property Like Never Before</h2>
      <p class="text-lg md:text-2xl mb-4">Drone Photography • Interior Styling • Airbnb Boost • Luxury Showcases</p>
      <a href="#contact" class="inline-block px-8 py-3 bg-blue-600 hover:bg-blue-700 rounded-xl font-semibold btn-hover">Book Your Package Today</a>
      <div class="mt-4 text-sm md:text-base">
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
        Turn Your Property into a Showstopper with Steph’s Drone & Revamping Services
At Steph’s Drone & Revamping Services, we don’t just take photos we create experiences that make your property unforgettable. Our expert team combines breathtaking drone aerial shots, polished interior and exterior photography, and professional property styling to ensure your listings capture attention, attract buyers or renters, and stand out in any market.
Whether you’re selling a home, boosting your Airbnb bookings, or showcasing a commercial space, we bring creativity, precision, and professionalism to every project. From the first click to the final image, we handle everything seamlessly, making the process fast, stress free, and impactful.
Why choose us?
Highlight your property’s best features with stunning visuals.
Make listings irresistible to potential buyers or renters.
Enjoy a stress free, professional service from start to finish.
Don’t just list your property make it unforgettable. Book your package today and let us turn your space into a visual masterpiece that sells.
      </p>
    </div>
  </section>

  <!-- Packages -->
  <section id="pricing" class="py-20 px-6 bg-gray-50">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-12">Packages</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
        <!-- Packages as in your original HTML -->
        <!-- Basic, Premium, Platinum, Event Package, Custom Quote -->
        <!-- [KEEP ALL PACKAGE CARDS AS IN YOUR ORIGINAL HTML] -->
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-20 px-6 bg-white">
    <div class="max-w-3xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-8">Get in Touch</h2>
      <form action="https://formsubmit.co/stephsdronerevampingservices@gmail.com" method="POST" class="space-y-6 bg-gray-50 p-8 rounded-2xl shadow">
        <div>
          <label class="block text-sm font-medium">Name</label>
          <input type="text" name="name" required class="w-full mt-2 px-4 py-3 border rounded-xl focus:ring-2 focus:ring-blue-500" />
        </div>
        <div>
          <label class="block text-sm font-medium">Email</label>
          <input type="email" name="email" required class="w-full mt-2 px-4 py-3 border rounded-xl focus:ring-2 focus:ring-blue-500" />
        </div>
        <div>
          <label class="block text-sm font-medium">Phone</label>
          <input type="text" name="phone" class="w-full mt-2 px-4 py-3 border rounded-xl focus:ring-2 focus:ring-blue-500" />
        </div>
        <div>
          <label class="block text-sm font-medium">Interested In</label>
          <select id="interest" name="interest" class="w-full mt-2 px-4 py-3 border rounded-xl focus:ring-2 focus:ring-blue-500">
            <option value="Basic — $50,000">Basic — $50,000</option>
            <option value="Premium — $80,000" selected>Premium — $80,000</option>
            <option value="Platinum — $100,000">Platinum — $100,000</option>
            <option value="Event Package — $120,000">Event Package — $120,000</option>
            <option value="Custom Quote">Custom Quote</option>
          </select>
        </div>
        <div>
          <label class="block text-sm font-medium">Message</label>
          <textarea name="message" rows="4" class="w-full mt-2 px-4 py-3 border rounded-xl focus:ring-2 focus:ring-blue-500"></textarea>
        </div>
        <input type="hidden" name="package" id="selectedPackage" value="Premium — $80,000">
        <button type="submit" class="w-full px-6 py-3 bg-blue-600 hover:bg-blue-700 text-white rounded-xl font-medium btn-hover">Send Message</button>
      </form>
    </div>
  </section>

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

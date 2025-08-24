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

    /* Floating drones */
    .drone {
      position: absolute;
      width: 40px;
      height: 40px;
      opacity: 0.3;
      background: url('https://cdn-icons-png.flaticon.com/512/688/688115.png') no-repeat center center;
      background-size: contain;
      animation: floatDrone linear infinite;
    }
    @keyframes floatDrone {
      0% { transform: translate(0,0) rotate(0deg); }
      50% { transform: translate(30px, -40px) rotate(20deg); }
      100% { transform: translate(0,0) rotate(0deg); }
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
    <div class="drone top-20 left-10 animate-[floatDrone_12s_infinite]"></div>
    <div class="drone top-32 right-16 animate-[floatDrone_15s_infinite]"></div>
    <div class="drone top-40 left-1/2 animate-[floatDrone_18s_infinite]"></div>
    <div class="drone bottom-24 right-32 animate-[floatDrone_20s_infinite]"></div>
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
        <img src="https://images.unsplash.com/photo-1580584124513-cb417a5b0a43?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Drone aerial Jamaica">
        <img src="https://images.unsplash.com/photo-1560185127-6fcb9f5bdebe?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Luxury villa Jamaica">
        <img src="https://images.unsplash.com/photo-1581091012184-8727e3267d8d?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Landscape Jamaica">
      </div>
    </div>
  </section>

  <!-- Packages -->
  <section id="pricing" class="py-20 px-6 bg-gray-50">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-12">Packages</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">

        <!-- Basic -->
        <div class="package-card rounded-2xl border shadow p-6 flex flex-col cursor-pointer" data-package="Basic — $50,000">
          <h3 class="text-2xl font-bold">Basic</h3>
          <p class="mt-2 text-gray-600">Perfect for quick listings and small spaces.</p>
          <p class="mt-4 text-2xl md:text-3xl font-bold text-blue-600">$50,000</p>
          <ul class="mt-4 space-y-2 text-gray-700 flex-1 text-sm">
            <li>• 10–15 edited photos (int./ext.)</li>
            <li>• 3–5 aerial photos</li>
            <li>• Basic color correction</li>
            <li>• 3–5 day delivery</li>
          </ul>
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-gray-900 text-white rounded-xl hover:bg-black text-sm btn-hover" data-package="Basic — $50,000">Book Basic</button>
        </div>

        <!-- Premium -->
        <div class="package-card rounded-2xl border shadow p-6 flex flex-col cursor-pointer active-package" data-package="Premium — $80,000">
          <div class="inline-block px-2 py-1 text-xs bg-blue-600 text-white rounded-full">Most Popular</div>
          <h3 class="text-2xl font-bold mt-2">Premium</h3>
          <p class="mt-1 text-gray-600">Ideal for standout listings & Airbnb.</p>
          <p class="mt-4 text-2xl md:text-3xl font-bold text-blue-600">$80,000</p>
          <ul class="mt-4 space-y-2 text-gray-700 flex-1 text-sm">
            <li>• 20–30 edited photos (int./ext.)</li>
            <li>• 8–12 aerial photos</li>
            <li>• 15–30s vertical video clip</li>
            <li>• Next-day preview</li>
          </ul>
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-blue-600 text-white rounded-xl hover:bg-blue-700 text-sm btn-hover" data-package="Premium — $80,000">Book Premium</button>
        </div>

        <!-- Platinum -->
        <div class="package-card rounded-2xl border shadow p-6 flex flex-col cursor-pointer" data-package="Platinum — $100,000">
          <h3 class="text-2xl font-bold">Platinum</h3>
          <p class="mt-2 text-gray-600">For luxury listings, events, and campaigns.</p>
          <p class="mt-4 text-2xl md:text-3xl font-bold text-blue-600">$100,000</p>
          <ul class="mt-4 space-y-2 text-gray-700 flex-1 text-sm">
            <li>• 35–50 edited photos (int./ext.)</li>
            <li>• 15–25 aerial photos</li>
            <li>• 60–90s highlight video</li>
            <li>• On-site styling & staging support</li>
          </ul>
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-gray-900 text-white rounded-xl hover:bg-black text-sm btn-hover" data-package="Platinum — $100,000">Book Platinum</button>
        </div>

        <!-- Event Package -->
        <div class="package-card rounded-2xl border shadow p-6 flex flex-col cursor-pointer" data-package="Event Package — $120,000">
          <h3 class="text-2xl font-bold">Event Package</h3>
          <p class="mt-2 text-gray-600">Perfect for weddings, parties & special events.</p>
          <p class="mt-4 text-2xl md:text-3xl font-bold text-blue-600">$120,000</p>
          <ul class="mt-4 space-y-2 text-gray-700 flex-1 text-sm">
            <li>• Full drone coverage of event</li>
            <li>• Professional ground photography</li>
            <li>• Highlight video included</li>
            <li>• 7–10 day delivery</li>
          </ul>
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-gray-900 text-white rounded-xl hover:bg-black text-sm btn-hover" data-package="Event Package — $120,000">Book Event Package</button>
        </div>

        <!-- Custom Quote -->
        <div class="package-card rounded-2xl border shadow p-6 flex flex-col cursor-pointer" data-package="Custom Quote">
          <h3 class="text-2xl font-bold">Custom Quote</h3>
          <p class="mt-2 text-gray-600">Don’t see a package that fits? Get a personalized quote.</p>
          <p class="mt-4 text-2xl md:text-3xl font-bold text-blue-600">—</p>
          <ul class="mt-4 space-y-2 text-gray-700 flex-1 text-sm">
            <li>• Tailored to your needs</li>
            <li>• Flexible services</li>
            <li>• Custom pricing</li>
          </ul>
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-gray-600 text-white rounded-xl hover:bg-gray-700 text-sm btn-hover" data-package="Custom Quote">Request Quote</button>
        </div>

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

  <!-- Script -->
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

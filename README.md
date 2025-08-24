# stephs-drone-revamping 
  FILE: index.html
  Steph’s Drone & Revamping Services — Single-page website
  Notes:
  • Update package prices inside the Pricing section (look for PRICE_HERE).
  • Contact form uses FormSubmit → sends directly to your Gmail and redirects to thank-you.html
========================== -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Steph’s Drone & Revamping Services</title>
  <meta name="description" content="Stunning drone shots, interior/exterior photography, and property revamping for real estate, Airbnb, events, and commercial spaces." />
  <meta property="og:title" content="Steph’s Drone & Revamping Services" />
  <meta property="og:description" content="Aerial visuals + property revamps that make every space stand out." />
  <meta property="og:type" content="website" />
  <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 128 128'%3E%3Ctext y='1em' font-size='96'%3E%F0%9F%9A%81%3C/text%3E%3C/svg%3E" />
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* Soft fade-in on scroll */
    .reveal { opacity: 0; transform: translateY(16px); transition: opacity .6s ease, transform .6s ease; }
    .reveal.show { opacity: 1; transform: translateY(0); }
    /* Glass card */
    .glass { background: rgba(255,255,255,.85); backdrop-filter: blur(8px); }
  </style>
  <script>
    // Intersection Observer to reveal elements on scroll
    document.addEventListener('DOMContentLoaded', () => {
      const io = new IntersectionObserver((entries) => {
        entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('show'); });
      }, { threshold: 0.15 });
      document.querySelectorAll('.reveal').forEach(el => io.observe(el));
    });

    // Contact form: sending state + redirect handled by hidden _next
    function handleSubmit(event) {
      event.preventDefault();
      const form = event.target;
      const btn = form.querySelector('button[type="submit"]');
      const original = btn.innerHTML;
      btn.disabled = true; btn.innerHTML = 'Sending…';
      const data = new FormData(form);
      fetch(form.action, { method: form.method, body: data, headers: { 'Accept': 'application/json' }})
        .then(r => {
          if (r.ok) { window.location.href = form.querySelector('input[name="_next"]').value; }
          else throw new Error('Submission failed');
        })
        .catch(() => { alert('Oops! Something went wrong. Please try again.'); btn.disabled = false; btn.innerHTML = original; });
    }
  </script>
</head>
<body class="bg-gray-50 text-gray-900 selection:bg-blue-600 selection:text-white">
  <!-- Nav -->
  <header class="fixed inset-x-0 top-0 z-50">
    <nav class="max-w-7xl mx-auto flex items-center justify-between py-4 px-6 bg-white/80 backdrop-blur-md shadow-sm rounded-b-2xl">
      <a href="#top" class="font-extrabold text-xl tracking-tight">Steph’s Drone <span class="text-blue-600">& Revamping</span></a>
      <div class="hidden md:flex items-center gap-6 text-sm font-medium">
        <a href="#services" class="hover:text-blue-600">Services</a>
        <a href="#portfolio" class="hover:text-blue-600">Portfolio</a>
        <a href="#pricing" class="hover:text-blue-600">Packages</a>
        <a href="#about" class="hover:text-blue-600">About</a>
        <a href="#contact" class="px-4 py-2 rounded-xl bg-blue-600 text-white hover:bg-blue-700">Book Now</a>
      </div>
      <a href="#contact" class="md:hidden inline-flex items-center px-3 py-2 rounded-xl bg-blue-600 text-white">Book</a>
    </nav>
  </header>

  <!-- Hero -->
  <section id="top" class="relative min-h-[92vh] grid place-items-center overflow-hidden">
    <img src="https://images.unsplash.com/photo-1473181488821-2d23949a045a?q=80&w=2400&auto=format&fit=crop" alt="Aerial of modern villa and pool" class="absolute inset-0 w-full h-full object-cover" />
    <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/30 to-black/10"></div>
    <div class="relative z-10 max-w-4xl mx-auto text-center px-6 text-white reveal">
      <h1 class="text-4xl md:text-6xl font-extrabold leading-tight">Steph’s Drone & Revamping Services</h1>
      <p class="mt-4 text-lg md:text-xl text-white/90">We capture breathtaking drone shots and deliver modern property revamps that make real estate, events, and landscapes unforgettable.</p>
      <div class="mt-8 flex flex-col sm:flex-row gap-3 justify-center">
        <a href="#portfolio" class="px-6 py-3 rounded-2xl bg-white/95 text-gray-900 font-semibold hover:bg-white">See Work</a>
        <a href="#contact" class="px-6 py-3 rounded-2xl bg-blue-600 font-semibold hover:bg-blue-700">Get a Quote</a>
      </div>
      <div class="mt-8 text-sm text-white/80">Instagram: <a class="underline hover:text-white" target="_blank" href="https://www.instagram.com/stephsdronerevampingservices?igsh=OW5yMnFnaGkzMmx4">@stephsdronerevampingservices</a> • Email: <a class="underline hover:text-white" href="mailto:stephsdronerevampingservices@gmail.com">stephsdronerevampingservices@gmail.com</a></div>
    </div>
  </section>

  <!-- Services -->
  <section id="services" class="py-20 px-6 bg-white">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 reveal">What We Do</h2>
      <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div class="glass rounded-2xl p-6 shadow reveal">
          <h3 class="text-xl font-semibold mb-2">Drone Photography & Videography</h3>
          <p class="text-gray-600">Aerial visuals that highlight architecture, land, and ambiance for listings, events, and marketing.</p>
        </div>
        <div class="glass rounded-2xl p-6 shadow reveal">
          <h3 class="text-xl font-semibold mb-2">Interior & Exterior Photography</h3>
          <p class="text-gray-600">Crisp, well-lit shots that show every angle — perfect for Airbnb, real estate, and commercial spaces.</p>
        </div>
        <div class="glass rounded-2xl p-6 shadow reveal">
          <h3 class="text-xl font-semibold mb-2">Property Revamping</h3>
          <p class="text-gray-600">Staging, styling, and light makeovers to create modern, welcoming spaces that attract buyers and guests.</p>
        </div>
      </div>
      <p class="max-w-4xl mx-auto mt-10 text-center text-gray-700 reveal">Steph’s Drone & Revamping Services is your go‑to for stunning visuals and property transformations. From real estate listings and Airbnb rentals to private estates and commercial spaces, our imagery makes every property stand out. We combine creativity, technology, and design to deliver results that leave a lasting impression.</p>
    </div>
  </section>

  <!-- Portfolio -->
  <section id="portfolio" class="py-20 px-6 bg-gray-50">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 reveal">Portfolio Highlights</h2>
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <figure class="overflow-hidden rounded-2xl shadow reveal"><img class="w-full h-72 object-cover hover:scale-105 transition" src="https://images.unsplash.com/photo-1494526585095-c41746248156?q=80&w=1600&auto=format&fit=crop" alt="Airbnb interior living room" /></figure>
        <figure class="overflow-hidden rounded-2xl shadow reveal"><img class="w-full h-72 object-cover hover:scale-105 transition" src="https://images.unsplash.com/photo-1505693416388-ac5ce068fe85?q=80&w=1600&auto=format&fit=crop" alt="Coastal landscape drone shot" /></figure>
        <figure class="overflow-hidden rounded-2xl shadow reveal"><img class="w-full h-72 object-cover hover:scale-105 transition" src="https://images.unsplash.com/photo-1484154218962-a197022b5858?q=80&w=1600&auto=format&fit=crop" alt="Modern home exterior at dusk" /></figure>
        <figure class="overflow-hidden rounded-2xl shadow reveal"><img class="w-full h-72 object-cover hover:scale-105 transition" src="https://images.unsplash.com/photo-1479705879471-65f3457ebd39?q=80&w=1600&auto=format&fit=crop" alt="Mountain landscape aerial" /></figure>
        <figure class="overflow-hidden rounded-2xl shadow reveal"><img class="w-full h-72 object-cover hover:scale-105 transition" src="https://images.unsplash.com/photo-1459535653751-d571815e906b?q=80&w=1600&auto=format&fit=crop" alt="Event venue from above" /></figure>
        <figure class="overflow-hidden rounded-2xl shadow reveal"><img class="w-full h-72 object-cover hover:scale-105 transition" src="https://images.unsplash.com/photo-1499951360447-b19be8fe80f5?q=80&w=1600&auto=format&fit=crop" alt="Styled bedroom Airbnb" /></figure>
      </div>
    </div>
  </section>

  <!-- Pricing / Packages -->
  <section id="pricing" class="py-20 px-6 bg-white">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 reveal">Packages</h2>
      <div class="grid md:grid-cols-3 gap-6">
        <!-- Basic -->
        <div class="rounded-2xl border shadow p-8 reveal">
          <h3 class="text-2xl font-bold">Basic</h3>
          <p class="mt-2 text-gray-600">Perfect for quick listings and small spaces.</p>
          <p class="mt-6 text-4xl font-extrabold">$50,000</p>
          <ul class="mt-6 space-y-2 text-gray-700">
            <li>• 10–15 edited photos (int./ext.)</li>
            <li>• 3–5 aerial photos</li>
            <li>• Basic color correction</li>
            <li>• 3–5 day delivery</li>
          </ul>
          <a href="#contact" class="mt-8 inline-block px-5 py-3 bg-gray-900 text-white rounded-xl hover:bg-black">Book Basic</a>
        </div>
        <!-- Premium -->
        <div class="rounded-2xl border-2 border-blue-600 shadow-lg p-8 reveal">
          <div class="inline-block px-3 py-1 text-xs bg-blue-600 text-white rounded-full">Most Popular</div>
          <h3 class="text-2xl font-bold mt-3">Premium</h3>
          <p class="mt-2 text-gray-600">Ideal for standout listings & Airbnb.</p>
          <p class="mt-6 text-4xl font-extrabold">$80,000</p>
          <ul class="mt-6 space-y-2 text-gray-700">
            <li>• 20–30 edited photos (int./ext.)</li>
            <li>• 8–12 aerial photos</li>
            <li>• 15–30s vertical video clip</li>
            <li>• Next‑day preview</li>
          </ul>
          <a href="#contact" class="mt-8 inline-block px-5 py-3 bg-blue-600 text-white rounded-xl hover:bg-blue-700">Book Premium</a>
        </div>
        <!-- Platinum -->
        <div class="rounded-2xl border shadow p-8 reveal">
          <h3 class="text-2xl font-bold">Platinum</h3>
          <p class="mt-2 text-gray-600">For luxury listings, events, and campaigns.</p>
          <p class="mt-6 text-4xl font-extrabold">$100,000</p>
          <ul class="mt-6 space-y-2 text-gray-700">
            <li>• 35–50 edited photos (int./ext.)</li>
            <li>• 15–25 aerial photos</li>
            <li>• 60–90s highlight video</li>
            <li>• On‑site styling & staging support</li>
          </ul>
          <a href="#contact" class="mt-8 inline-block px-5 py-3 bg-gray-900 text-white rounded-xl hover:bg-black">Book Platinum</a>
        </div>
      </div>
      <p class="text-center text-sm text-gray-500 mt-6">Need something custom? <a href="#contact" class="text-blue-700 underline">Contact us</a> for a tailored quote.</p>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="py-20 px-6 bg-gray-50">
    <div class="max-w-5xl mx-auto reveal">
      <h2 class="text-3xl md:text-4xl font-bold mb-6">About Us</h2>
      <p class="text-gray-700 leading-relaxed">We specialize in drone photography and videography, capturing breathtaking aerial shots that highlight the unique features of every property. From real estate listings and Airbnb rentals to private estates and commercial spaces, we also create polished interior and exterior photography to showcase your space from every angle. Beyond imagery, our property revamping service adds modern styling and creative staging to elevate appeal and performance. Whether you’re marketing a home for sale, boosting Airbnb bookings, or promoting an event, our team brings your vision to life with professionalism, creativity, and excellence.</p>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-20 px-6 bg-gradient-to-b from-white to-blue-50">
    <div class="max-w-4xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-10 reveal">Get in Touch</h2>
      <div class="grid md:grid-cols-2 gap-6 items-start">
        <form action="https://formsubmit.co/stephsdronerevampingservices@gmail.com" method="POST" onsubmit="handleSubmit(event)" class="bg-white rounded-2xl shadow p-6 md:p-8 reveal">
          <!-- FormSubmit options -->
          <input type="hidden" name="_captcha" value="false" />
          <input type="hidden" name="_next" value="thank-you.html" />
          <input type="hidden" name="_subject" value="New Booking Inquiry — Steph’s Drone & Revamping" />

          <div class="grid sm:grid-cols-2 gap-4">
            <div>
              <label class="block text-sm font-medium mb-1">Name</label>
              <input name="name" required class="w-full rounded-xl border p-3 focus:outline-none focus:ring-2 focus:ring-blue-600" placeholder="Your name" />
            </div>
            <div>
              <label class="block text-sm font-medium mb-1">Email</label>
              <input type="email" name="email" required class="w-full rounded-xl border p-3 focus:outline-none focus:ring-2 focus:ring-blue-600" placeholder="you@email.com" />
            </div>
          </div>

          <div class="mt-4 grid sm:grid-cols-2 gap-4">
            <div>
              <label class="block text-sm font-medium mb-1">Phone (optional)</label>
              <input name="phone" class="w-full rounded-xl border p-3 focus:outline-none focus:ring-2 focus:ring-blue-600" placeholder="(xxx) xxx-xxxx" />
            </div>
            <div>
              <label class="block text-sm font-medium mb-1">Interested In</label>
              <select name="service" class="w-full rounded-xl border p-3 bg-white focus:outline-none focus:ring-2 focus:ring-blue-600">
                <option>Drone Photo/Video</option>
                <option>Interior Photography</option>
                <option>Exterior Photography</option>
                <option>Property Revamping</option>
                <option>Custom Package</option>
              </select>
            </div>
          </div>

          <div class="mt-4">
            <label class="block text-sm font-medium mb-1">Message</label>
            <textarea name="message" required class="w-full rounded-xl border p-3 h-28 focus:outline-none focus:ring-2 focus:ring-blue-600" placeholder="Tell us about your property or event…"></textarea>
          </div>

          <button type="submit" class="mt-6 w-full bg-blue-600 text-white font-semibold rounded-xl py-3 hover:bg-blue-700">Send Message</button>
          <p class="text-xs text-gray-500 mt-3">By submitting, you agree to be contacted about your inquiry.</p>
        </form>

        <aside class="reveal bg-white rounded-2xl shadow p-6 md:p-8">
          <h3 class="text-xl font-semibold">Contact Details</h3>
          <p class="mt-2 text-gray-700">We usually reply within 24 hours.</p>
          <div class="mt-4 space-y-2 text-gray-800">
            <p>📧 Email: <a class="text-blue-700 underline" href="mailto:stephsdronerevampingservices@gmail.com">stephsdronerevampingservices@gmail.com</a></p>
            <p>📸 Instagram: <a class="text-blue-700 underline" target="_blank" href="https://www.instagram.com/stephsdronerevampingservices?igsh=OW5yMnFnaGkzMmx4">@stephsdronerevampingservices</a></p>
          </div>
          <div class="mt-6 text-sm text-gray-600">
            <p>Serving: Real estate agents, Airbnb hosts, homeowners, and event planners.</p>
            <p class="mt-1">Available for sunrise/sunset shoots upon request.</p>
          </div>
        </aside>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="py-8 text-center bg-gray-900 text-gray-300">
    <p>© <span id="y"></span> Steph’s Drone & Revamping Services. All rights reserved.</p>
  </footer>

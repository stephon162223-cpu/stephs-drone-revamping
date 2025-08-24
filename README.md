<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Steph’s Drone & Revamping Services</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    .active-package {
      border: 2px solid #2563eb;
      box-shadow: 0 0 10px rgba(37, 99, 235, 0.4);
    }
  </style>
</head>
<body class="font-sans text-gray-900">

  <!-- Hero -->
  <section class="relative bg-gray-900 text-white py-24 px-6 text-center">
    <h1 class="text-4xl md:text-6xl font-bold">Steph’s Drone & Revamping Services</h1>
    <p class="mt-4 text-lg md:text-xl max-w-2xl mx-auto">
      Capturing stunning aerial views, professional photography, and creative revamping for your property or event.
    </p>
    <a href="#pricing" class="mt-8 inline-block px-6 py-3 bg-blue-600 hover:bg-blue-700 rounded-xl text-lg font-medium">View Packages</a>
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
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-gray-900 text-white rounded-xl hover:bg-black text-sm" data-package="Basic — $50,000">Book Basic</button>
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
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-blue-600 text-white rounded-xl hover:bg-blue-700 text-sm" data-package="Premium — $80,000">Book Premium</button>
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
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-gray-900 text-white rounded-xl hover:bg-black text-sm" data-package="Platinum — $100,000">Book Platinum</button>
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
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-gray-900 text-white rounded-xl hover:bg-black text-sm" data-package="Event Package — $120,000">Book Event Package</button>
        </div>

        <!-- Custom Quote -->
        <div class="package-card rounded-2xl border shadow p-6 flex flex-col cursor-pointer" data-package="Custom Quote">
          <h3 class="text-2xl font-bold">Custom Quote</h3>
          <p class="mt-2 text-gray-600">Don’t see a package that fits? Get a personalized quote for your project.</p>
          <p class="mt-4 text-2xl md:text-3xl font-bold text-blue-600">—</p>
          <ul class="mt-4 space-y-2 text-gray-700 flex-1 text-sm">
            <li>• Tailored to your needs</li>
            <li>• Flexible services</li>
            <li>• Custom pricing</li>
          </ul>
          <button type="button" class="book-btn mt-4 px-4 py-2 bg-gray-600 text-white rounded-xl hover:bg-gray-700 text-sm" data-package="Custom Quote">Request Quote</button>
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

        <!-- Hidden input to send selected package -->
        <input type="hidden" name="package" id="selectedPackage" value="Premium — $80,000">

        <button type="submit" class="w-full px-6 py-3 bg-blue-600 hover:bg-blue-700 text-white rounded-xl font-medium">Send Message</button>
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
        // remove highlight
        packageCards.forEach(c => c.classList.remove("active-package"));
        card.classList.add("active-package");

        // set values
        const selected = card.dataset.package;
        packageInput.value = selected;
        interestDropdown.value = selected;
      });
    });

    // Book button click = auto-select package
    document.querySelectorAll(".book-btn").forEach(btn => {
      btn.addEventListener("click", () => {
        const selected = btn.dataset.package;
        packageInput.value = selected;
        interestDropdown.value = selected;

        // highlight correct card
        packageCards.forEach(c => {
          c.classList.toggle("active-package", c.dataset.package === selected);
        });

        // scroll to contact form
        document.querySelector("#contact").scrollIntoView({ behavior: "smooth" });
      });
    });
  </script>
</body>
</html>

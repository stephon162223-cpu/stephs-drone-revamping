<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Steph’s Drone & Revamping Services</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <style>
    .active {
      border: 2px solid #2563eb;
      box-shadow: 0 0 12px rgba(37,99,235,0.6);
    }
  </style>
</head>
<body class="bg-gray-50 text-gray-900">

  <!-- Header -->
  <header class="py-6 bg-white shadow">
    <div class="max-w-7xl mx-auto flex justify-between items-center px-6">
      <h1 class="text-2xl font-bold">Steph’s Drone & Revamping Services</h1>
      <a href="#contact" class="px-4 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700">Book Now</a>
    </div>
  </header>

  <!-- Hero -->
  <section class="py-20 px-6 text-center bg-gradient-to-r from-blue-500 to-indigo-600 text-white">
    <h2 class="text-4xl md:text-5xl font-bold">Bring Your Property to Life</h2>
    <p class="mt-4 text-lg">Professional drone shots, real estate media, and revamping services.</p>
    <a href="#pricing" class="mt-8 inline-block px-6 py-3 bg-white text-blue-600 font-semibold rounded-xl hover:bg-gray-100">View Packages</a>
  </section>

  <!-- Pricing -->
  <section id="pricing" class="py-20 px-6 bg-white">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-12">Packages</h2>
      <div class="grid md:grid-cols-3 gap-6">

        <!-- Basic -->
        <div class="package-card rounded-2xl border shadow p-8 cursor-pointer" data-package="Basic — $50,000">
          <h3 class="text-2xl font-bold">Basic</h3>
          <p class="mt-2 text-gray-600">Perfect for quick listings and small spaces.</p>
          <p class="mt-6 text-4xl font-extrabold">$50,000</p>
          <ul class="mt-6 space-y-2 text-gray-700">
            <li>• 10–15 edited photos (int./ext.)</li>
            <li>• 3–5 aerial photos</li>
            <li>• Basic color correction</li>
            <li>• 3–5 day delivery</li>
          </ul>
          <button type="button" class="book-btn mt-8 inline-block px-5 py-3 bg-gray-900 text-white rounded-xl hover:bg-black" data-package="Basic — $50,000">Book Basic</button>
        </div>

        <!-- Premium -->
        <div class="package-card rounded-2xl border shadow p-8 cursor-pointer active" data-package="Premium — $80,000">
          <div class="inline-block px-3 py-1 text-xs bg-blue-600 text-white rounded-full">Most Popular</div>
          <h3 class="text-2xl font-bold mt-3">Premium</h3>
          <p class="mt-2 text-gray-600">Ideal for standout listings & Airbnb.</p>
          <p class="mt-6 text-4xl font-extrabold">$80,000</p>
          <ul class="mt-6 space-y-2 text-gray-700">
            <li>• 20–30 edited photos (int./ext.)</li>
            <li>• 8–12 aerial photos</li>
            <li>• 15–30s vertical video clip</li>
            <li>• Next-day preview</li>
          </ul>
          <button type="button" class="book-btn mt-8 inline-block px-5 py-3 bg-blue-600 text-white rounded-xl hover:bg-blue-700" data-package="Premium — $80,000">Book Premium</button>
        </div>

        <!-- Platinum -->
        <div class="package-card rounded-2xl border shadow p-8 cursor-pointer" data-package="Platinum — $100,000">
          <h3 class="text-2xl font-bold">Platinum</h3>
          <p class="mt-2 text-gray-600">For luxury listings, events, and campaigns.</p>
          <p class="mt-6 text-4xl font-extrabold">$100,000</p>
          <ul class="mt-6 space-y-2 text-gray-700">
            <li>• 35–50 edited photos (int./ext.)</li>
            <li>• 15–25 aerial photos</li>
            <li>• 60–90s highlight video</li>
            <li>• On-site styling & staging support</li>
          </ul>
          <button type="button" class="book-btn mt-8 inline-block px-5 py-3 bg-gray-900 text-white rounded-xl hover:bg-black" data-package="Platinum — $100,000">Book Platinum</button>
        </div>

      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-20 px-6 bg-gray-100">
    <div class="max-w-3xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-8">Get in Touch</h2>
      <form id="bookingForm" action="https://formsubmit.co/YOUR_EMAIL_HERE" method="POST" class="bg-white shadow-lg rounded-2xl p-8 space-y-6">
        
        <!-- Hidden package input -->
        <input type="hidden" name="package" id="selectedPackage" value="Premium — $80,000">
        <input type="hidden" name="_captcha" value="false">

        <div>
          <label class="block font-medium">Name</label>
          <input type="text" name="name" required class="w-full mt-2 p-3 border rounded-lg">
        </div>

        <div>
          <label class="block font-medium">Email</label>
          <input type="email" name="email" required class="w-full mt-2 p-3 border rounded-lg">
        </div>

        <div>
          <label class="block font-medium">Interested In</label>
          <select name="interest" id="interest" required class="w-full mt-2 p-3 border rounded-lg">
            <option value="">Select a package</option>
            <option value="Basic — $50,000">Basic — $50,000</option>
            <option value="Premium — $80,000" selected>Premium — $80,000</option>
            <option value="Platinum — $100,000">Platinum — $100,000</option>
          </select>
        </div>

        <div>
          <label class="block font-medium">Message</label>
          <textarea name="message" id="message" rows="4" class="w-full mt-2 p-3 border rounded-lg">I’m interested in the Premium — $80,000 package.</textarea>
        </div>

        <button type="submit" class="w-full px-6 py-3 bg-blue-600 text-white rounded-lg font-semibold hover:bg-blue-700">Send Booking</button>
      </form>

      <!-- Thank You Message -->
      <div id="thankYou" class="hidden text-center bg-white shadow-lg rounded-2xl p-12">
        <h3 class="text-2xl font-bold text-green-600">✅ Thank You!</h3>
        <p class="mt-4">Your booking request has been sent successfully. We’ll get back to you soon!</p>
        <a href="#pricing" class="mt-6 inline-block px-5 py-3 bg-blue-600 text-white rounded-xl hover:bg-blue-700">Back to Packages</a>
      </div>
    </div>
  </section>

  <!-- Script -->
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const packageCards = document.querySelectorAll('.package-card');
      const packageInput = document.querySelector('#selectedPackage');
      const interestDropdown = document.querySelector('#interest');
      const messageBox = document.querySelector('#message');
      const bookButtons = document.querySelectorAll('.book-btn');
      const form = document.querySelector('#bookingForm');
      const thankYou = document.querySelector('#thankYou');

      function selectPackage(selected) {
        // highlight
        packageCards.forEach(c => {
          c.classList.remove('active');
          if (c.dataset.package === selected) c.classList.add('active');
        });

        // set values
        packageInput.value = selected;
        interestDropdown.value = selected;
        messageBox.value = `I’m interested in the ${selected} package.`;

        // scroll to form
        document.querySelector('#contact').scrollIntoView({behavior: "smooth"});
      }

      packageCards.forEach(card => {
        card.addEventListener('click', () => selectPackage(card.dataset.package));
      });

      bookButtons.forEach(btn => {
        btn.addEventListener('click', () => selectPackage(btn.dataset.package));
      });

      // Show thank you message after submission
      form.addEventListener('submit', function(e) {
        e.preventDefault();
        const data = new FormData(form);
        fetch(form.action, { method: 'POST', body: data })
          .then(() => {
            form.classList.add('hidden');
            thankYou.classList.remove('hidden');
          })
          .catch(err => alert("Something went wrong. Please try again."));
      });
    });
  </script>

</body>
</html>

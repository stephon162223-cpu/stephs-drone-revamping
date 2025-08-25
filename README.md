<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Steph’s Drone & Revamping Services</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    html {
      scroll-behavior: smooth;
    }
    .package {
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .package:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 20px rgba(0,0,0,0.15);
    }
    .selected {
      border: 3px solid #2563eb;
      box-shadow: 0 0 20px rgba(37,99,235,0.5);
    }
    .portfolio-img {
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }
    .portfolio-img:hover {
      transform: scale(1.05);
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
    }
  </style>
</head>
<body class="font-sans text-gray-800">

  <!-- Navbar -->
  <header class="bg-white shadow fixed top-0 left-0 w-full z-50">
    <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
      <h1 class="text-2xl font-bold">Steph’s Drone & Revamping</h1>
      <nav class="space-x-6">
        <a href="#about" class="hover:text-blue-600">About</a>
        <a href="#portfolio" class="hover:text-blue-600">Portfolio</a>
        <a href="#pricing" class="hover:text-blue-600">Pricing</a>
        <a href="#contact" class="hover:text-blue-600">Contact</a>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <section class="h-screen flex items-center justify-center bg-gradient-to-r from-blue-600 to-indigo-700 text-white text-center px-6">
    <div>
      <h2 class="text-4xl md:text-6xl font-bold mb-4">Professional Drone & Revamping Services</h2>
      <p class="text-lg md:text-2xl mb-8">Capturing breathtaking aerial shots and transforming spaces across Jamaica</p>
      <a href="#pricing" class="bg-white text-blue-600 font-semibold px-6 py-3 rounded-full shadow hover:bg-gray-100">View Packages</a>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="py-20 px-6 bg-gray-50">
    <div class="max-w-5xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold mb-6">About Us</h2>
      <p class="text-lg leading-relaxed text-gray-700">
        At Steph’s Drone & Revamping Services, we specialize in capturing stunning aerial footage and enhancing property aesthetics. 
        From real estate and Airbnb showcases to breathtaking landscapes of Jamaica, our mission is to bring your vision to life. 
        With a commitment to quality and creativity, we deliver professional results that make your project stand out.
      </p>
    </div>
  </section>

  <!-- Portfolio -->
  <section id="portfolio" class="py-20 px-6 bg-gray-50">
    <div class="max-w-7xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold mb-12">Portfolio</h2>
      <div class="grid md:grid-cols-3 gap-6">
        <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Luxury villa in Jamaica">
        <img src="https://images.unsplash.com/photo-1600585153937-7c1c2eac9a7a?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Airbnb interior Jamaica">
        <img src="https://images.unsplash.com/photo-1580584126903-c17d41830450?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Drone aerial estate Jamaica">
        <img src="https://images.unsplash.com/photo-1524492449090-1a0642b6f3c2?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Jamaican landscape">
        <img src="https://images.unsplash.com/photo-1600607688970-7ec6a19670fe?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Modern apartment Kingston">
        <img src="https://images.unsplash.com/photo-1613490493576-7b8b1f6c4b4c?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" class="rounded-xl shadow portfolio-img" alt="Resort Montego Bay">
      </div>
    </div>
  </section>

  <!-- Pricing -->
  <section id="pricing" class="py-20 px-6">
    <div class="max-w-7xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold mb-12">Our Packages</h2>
      <div class="grid md:grid-cols-4 gap-6">
        <div class="package bg-white p-6 rounded-xl shadow hover:shadow-lg" data-package="Basic Package" data-price="$100">
          <h3 class="text-xl font-bold mb-4">Basic</h3>
          <p class="mb-4">Entry-level drone shots</p>
          <p class="font-semibold">$100</p>
        </div>
        <div class="package bg-white p-6 rounded-xl shadow hover:shadow-lg" data-package="Standard Package" data-price="$200">
          <h3 class="text-xl font-bold mb-4">Standard</h3>
          <p class="mb-4">Includes editing & enhancements</p>
          <p class="font-semibold">$200</p>
        </div>
        <div class="package bg-white p-6 rounded-xl shadow hover:shadow-lg selected" data-package="Premium Package" data-price="$350">
          <h3 class="text-xl font-bold mb-4">Premium</h3>
          <p class="mb-4">Full project coverage</p>
          <p class="font-semibold">$350</p>
        </div>
        <div class="package bg-white p-6 rounded-xl shadow hover:shadow-lg" data-package="Custom Quote" data-price="Varies">
          <h3 class="text-xl font-bold mb-4">Custom Quote</h3>
          <p class="mb-4">Tailored to your unique needs</p>
          <p class="font-semibold">Contact for price</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="py-20 px-6 bg-gray-50">
    <div class="max-w-3xl mx-auto text-center">
      <h2 class="text-3xl md:text-4xl font-bold mb-6">Get in Touch</h2>
      <p class="mb-8 text-gray-600">Fill out the form below and we’ll get back to you shortly.</p>
      <form action="https://formsubmit.co/stephsdronerevampingservices@gmail.com" method="POST" class="space-y-4 bg-white p-8 rounded-xl shadow">
        <input type="hidden" name="_subject" value="New Booking Request">
        <input type="hidden" name="_next" value="thank-you.html">
        <input type="hidden" id="selected-package" name="Selected Package" value="Premium Package - $350">

        <input type="text" name="name" placeholder="Your Name" required class="w-full border p-3 rounded">
        <input type="email" name="email" placeholder="Your Email" required class="w-full border p-3 rounded">
        <textarea name="message" placeholder="Your Message" rows="4" class="w-full border p-3 rounded"></textarea>

        <button type="submit" class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-blue-700">Send Message</button>
      </form>
    </div>
  </section>

  <footer class="py-6 bg-gray-800 text-center text-white">
    <p>&copy; 2025 Steph’s Drone & Revamping Services. All rights reserved.</p>
  </footer>

  <script>
    // Package selection
    const packages = document.querySelectorAll('.package');
    const hiddenInput = document.getElementById('selected-package');

    packages.forEach(pkg => {
      pkg.addEventListener('click', () => {
        packages.forEach(p => p.classList.remove('selected'));
        pkg.classList.add('selected');
        hiddenInput.value = pkg.getAttribute('data-package') + " - " + pkg.getAttribute('data-price');
      });
    });
  </script>

</body>
</html>

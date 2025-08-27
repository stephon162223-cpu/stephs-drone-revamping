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

    /* Promo cinematic video section */
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
      transform: scale(1);
      transition: opacity 1.5s ease-in-out, transform 20s ease-in-out;
    }
    .promo-slide.active {
      opacity: 1;
      transform: scale(1.1);
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
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100%;
      text-align: center;
      padding: 0 1.5rem;
      color: #fff;
    }
    .promo-content img {
      width: 150px;
      margin-bottom: 1rem;
    }
    .promo-caption {
      font-size: 1.5rem;
      font-weight: 600;
      margin-top: 0.5rem;
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 1s ease, transform 1s ease;
    }
    .promo-caption.active {
      opacity: 1;
      transform: translateY(0);
    }
    .promo-content h2 {
      font-size: 2.5rem;
      font-weight: 800;
      margin-bottom: 0.5rem;
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 1s ease, transform 1s ease;
    }
    .promo-content h2.active {
      opacity: 1;
      transform: translateY(0);
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

  <!-- Promo cinematic section -->
  <section id="promo">
    <img src="https://images.unsplash.com/photo-1568605114967-8130f3a36994?auto=format&fit=crop&w=1600&q=80" class="promo-slide active" alt="Jamaican property 1" data-caption="Drone Photography">
    <img src="https://images.unsplash.com/photo-1505691723518-41cb3c27f8aa?auto=format&fit=crop&w=1600&q=80" class="promo-slide" alt="Jamaican property 2" data-caption="Interior & Exterior Styling">
    <img src="https://images.unsplash.com/photo-1505691938895-1758d7feb511?auto=format&fit=crop&w=1600&q=80" class="promo-slide" alt="Jamaican property 3" data-caption="Boost Airbnb Bookings">
    <img src="https://images.unsplash.com/photo-1523217582562-09d0def993a6?auto=format&fit=crop&w=1600&q=80" class="promo-slide" alt="Jamaican property 4" data-caption="Luxury Property Showcases">
    
    <div class="promo-overlay"></div>

    <div class="promo-content">
      <img src="https://YOUR_LOGO_URL_HERE.png" alt="SDRS Logo">
      <h2 class="active">Experience Your Property Like Never Before</h2>
      <div class="promo-caption active">Drone Photography</div>
      <a href="#contact" class="mt-4 inline-block px-8 py-4 bg-blue-600 hover:bg-blue-700 text-white font-semibold rounded-xl shadow-lg btn-hover">
        Book Your Package Today
      </a>
      <div class="mt-4 text-gray-200 text-sm md:text-base">
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

  <!-- Packages and Contact remain unchanged -->

  <script>
    // Promo cinematic slides with captions
    const slides = document.querySelectorAll('.promo-slide');
    const caption = document.querySelector('.promo-caption');
    const title = document.querySelector('.promo-content h2');
    let currentSlide = 0;
    setInterval(() => {
      slides[currentSlide].classList.remove('active');
      currentSlide = (currentSlide + 1) % slides.length;
      slides[currentSlide].classList.add('active');
      // update caption
      caption.classList.remove('active');
      title.classList.remove('active');
      setTimeout(() => {
        caption.textContent = slides[currentSlide].dataset.caption;
        caption.classList.add('active');
        title.classList.add('active');
      }, 500);
    }, 7000); // 7 seconds per slide

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

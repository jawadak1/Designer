<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Jawad Ahmed — Portfolio</title>

  <!-- Tailwind Play CDN for quick use (no build step) -->
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* Add a few custom styles */
    :root {
      --brand: #ff7a00; /* orange */
    }
    .brand {
      color: var(--brand);
    }
    .brand-bg {
      background-color: var(--brand);
    }
    /* simple modal backdrop */
    .modal-backdrop {
      background: rgba(0,0,0,0.6);
    }
  </style>
</head>
<body class="bg-gray-50 text-gray-800 antialiased">

  <!-- NAV -->
  <header class="sticky top-0 z-30 bg-white/80 backdrop-blur-sm shadow-sm">
    <div class="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
      <a href="#" class="flex items-center gap-3">
        <div class="w-10 h-10 rounded-full brand-bg flex items-center justify-center text-white font-semibold">JA</div>
        <div>
          <div class="font-semibold">Jawad Ahmed</div>
          <div class="text-xs text-gray-500">Graphic Designer</div>
        </div>
      </a>

      <nav class="hidden md:flex gap-6 items-center text-sm">
        <a href="#work" class="hover:underline">Work</a>
        <a href="#about" class="hover:underline">About</a>
        <a href="#contact" class="hover:underline">Contact</a>
        <a href="#" class="px-3 py-1 rounded-md brand-bg text-white text-sm">Hire Me</a>
      </nav>

      <!-- mobile menu button -->
      <div class="md:hidden">
        <button id="mobileBtn" class="p-2 rounded-md hover:bg-gray-100">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none"
               viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round"
               stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/></svg>
        </button>
      </div>
    </div>
  </header>

  <!-- HERO -->
  <main class="max-w-6xl mx-auto px-4 py-12">
    <section class="grid md:grid-cols-2 gap-8 items-center">
      <div>
        <h1 class="text-4xl md:text-5xl font-bold mb-3">I design clean visual identities & digital experiences.</h1>
        <p class="text-gray-600 mb-6">I’m Jawad, a graphic designer specializing in branding, UI design, and visual storytelling. Below are selected projects — click any to view details.</p>

        <div class="flex gap-3">
          <a href="#work" class="inline-flex items-center gap-2 px-4 py-2 rounded-md border border-transparent brand-bg text-white">View Work</a>
          <a href="#contact" class="inline-flex items-center gap-2 px-4 py-2 rounded-md border border-gray-200">Contact</a>
          <a href="#" class="inline-flex items-center gap-2 px-4 py-2 rounded-md border border-gray-200">Download CV</a>
        </div>
      </div>

      <div class="hidden md:block">
        <div class="w-full h-80 rounded-lg overflow-hidden shadow-lg">
          <img src="https://images.unsplash.com/photo-1503602642458-232111445657?q=80&w=1400&auto=format&fit=crop&ixlib=rb-4.0.3&s=1a9b5ff2b8c9d2871d66d06b5b7c9d6b" alt="design" class="w-full h-full object-cover">
        </div>
      </div>
    </section>

    <!-- WORK / PORTFOLIO -->
    <section id="work" class="mt-16">
      <div class="flex items-center justify-between mb-6">
        <h2 class="text-2xl font-semibold">Selected Projects</h2>

        <!-- filters -->
        <div class="flex gap-2">
          <button class="filterBtn px-3 py-1 rounded-md text-sm bg-white border" data-filter="all">All</button>
          <button class="filterBtn px-3 py-1 rounded-md text-sm" data-filter="branding">Branding</button>
          <button class="filterBtn px-3 py-1 rounded-md text-sm" data-filter="ui">UI</button>
          <button class="filterBtn px-3 py-1 rounded-md text-sm" data-filter="illustration">Illustration</button>
        </div>
      </div>

      <div id="portfolioGrid" class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <!-- card 1 -->
        <article class="projectCard bg-white rounded-lg overflow-hidden shadow-sm cursor-pointer" data-cat="branding" data-title="Elegant Home Seller" data-desc="Brand identity for a real estate business: logo, color palette, business cards." data-images='["https://images.unsplash.com/photo-1494526585095-c41746248156?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=8f1b395d4b6f6a2e3b9f3e2c5a4a3e1c"]'>
          <div class="h-48 overflow-hidden">
            <img class="w-full h-full object-cover" src="https://images.unsplash.com/photo-1502673530728-f79b4cab31b1?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=e3a2cbd8ff8d3d86a3a3c2b8a3b6d8f1" alt="">
          </div>
          <div class="p-4">
            <div class="font-semibold">Elegant Home Seller</div>
            <div class="text-xs text-gray-500 mt-1">Branding</div>
          </div>
        </article>

        <!-- card 2 -->
        <article class="projectCard bg-white rounded-lg overflow-hidden shadow-sm cursor-pointer" data-cat="ui" data-title="Fintech App UI" data-desc="Mobile-first fintech UI: onboarding, dashboard, and transactions screens." data-images='["https://images.unsplash.com/photo-1556155092-490a1ba16284?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=3f2b7d8293f6e7c1e2b8d5c4a7b6d3e2"]'>
          <div class="h-48 overflow-hidden">
            <img class="w-full h-full object-cover" src="https://images.unsplash.com/photo-1542744095-fcf48d80b0fd?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=b3b1ea5c3f5d8f2d9d8f2c0e1e4b5a1a" alt="">
          </div>
          <div class="p-4">
            <div class="font-semibold">Fintech App UI</div>
            <div class="text-xs text-gray-500 mt-1">UI</div>
          </div>
        </article>

        <!-- card 3 -->
        <article class="projectCard bg-white rounded-lg overflow-hidden shadow-sm cursor-pointer" data-cat="illustration" data-title="Lahori Chillers Pack" data-desc="Food packaging and tray design for Lahori Chillers — bold colors, playful type." data-images='["https://images.unsplash.com/photo-1544025162-d76694265947?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=6e2b9c7f3a0d8f1e2c3b4a5d6f7e8a9b"]'>
          <div class="h-48 overflow-hidden">
            <img class="w-full h-full object-cover" src="https://images.unsplash.com/photo-1503602642458-232111445657?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=1a9b5ff2b8c9d2871d66d06b5b7c9d6b" alt="">
          </div>
          <div class="p-4">
            <div class="font-semibold">Lahori Chillers Pack</div>
            <div class="text-xs text-gray-500 mt-1">Illustration</div>
          </div>
        </article>

        <!-- more example cards (duplicate for demo) -->
        <article class="projectCard bg-white rounded-lg overflow-hidden shadow-sm cursor-pointer" data-cat="branding" data-title="Amniva Skincare" data-desc="Product label and social assets for a skincare brand." data-images='["https://images.unsplash.com/photo-1542831371-d531d36971e6?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=8b9a0d6f1c2e3b4a5c6d7e8f9a0b1c2d"]'>
          <div class="h-48 overflow-hidden">
            <img class="w-full h-full object-cover" src="https://images.unsplash.com/photo-1503602642458-232111445657?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=1a9b5ff2b8c9d2871d66d06b5b7c9d6b" alt="">
          </div>
          <div class="p-4">
            <div class="font-semibold">Amniva Skincare</div>
            <div class="text-xs text-gray-500 mt-1">Branding</div>
          </div>
        </article>

        <article class="projectCard bg-white rounded-lg overflow-hidden shadow-sm cursor-pointer" data-cat="ui" data-title="Portfolio Website UI" data-desc="A minimal portfolio UI concept with smooth interactions." data-images='["https://images.unsplash.com/photo-1523475496153-3d6ccf38a3d2?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=3c1234567890abcdef1234567890abcd"]'>
          <div class="h-48 overflow-hidden">
            <img class="w-full h-full object-cover" src="https://images.unsplash.com/photo-1542744095-fcf48d80b0fd?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=b3b1ea5c3f5d8f2d9d8f2c0e1e4b5a1a" alt="">
          </div>
          <div class="p-4">
            <div class="font-semibold">Portfolio Website UI</div>
            <div class="text-xs text-gray-500 mt-1">UI</div>
          </div>
        </article>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="mt-16 bg-white p-6 rounded-lg shadow-sm">
      <h3 class="text-xl font-semibold mb-3">About Me</h3>
      <div class="md:flex gap-6 items-start">
        <div class="w-36 h-36 rounded-lg overflow-hidden flex-shrink-0">
          <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?q=80&w=800&auto=format&fit=crop&ixlib=rb-4.0.3&s=0b1a2c3d4e5f6a7b8c9d0e1f2a3b4c5d" alt="profile" class="w-full h-full object-cover">
        </div>

        <div>
          <p class="text-gray-600">I craft identities, packaging, and interfaces with a focus on clarity and user-centered visuals. I use Illustrator, Photoshop, and Figma for design and prototyping.</p>

          <div class="mt-4 grid grid-cols-2 sm:grid-cols-4 gap-3">
            <div class="p-3 rounded border text-center">
              <div class="font-semibold">Branding</div>
              <div class="text-sm text-gray-500">Logo, Identity</div>
            </div>
            <div class="p-3 rounded border text-center">
              <div class="font-semibold">UI/UX</div>
              <div class="text-sm text-gray-500">Web & Mobile</div>
            </div>
            <div class="p-3 rounded border text-center">
              <div class="font-semibold">Packaging</div>
              <div class="text-sm text-gray-500">Print Ready</div>
            </div>
            <div class="p-3 rounded border text-center">
              <div class="font-semibold">Motion</div>
              <div class="text-sm text-gray-500">Basic Animations</div>
            </div>
          </div>

          <div class="mt-4">
            <a href="#" class="inline-block px-4 py-2 rounded-md brand-bg text-white">Download CV</a>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="mt-16">
      <div class="bg-white p-6 rounded-lg shadow-sm">
        <h3 class="text-xl font-semibold mb-4">Get in touch</h3>
        <form id="contactForm" class="grid gap-3 md:grid-cols-2">
          <input name="name" required placeholder="Your name" class="p-3 border rounded-md"/>
          <input name="email" type="email" required placeholder="Your email" class="p-3 border rounded-md"/>
          <input name="subject" placeholder="Subject" class="p-3 border rounded-md md:col-span-2"/>
          <textarea name="message" required placeholder="Message" rows="5" class="p-3 border rounded-md md:col-span-2"></textarea>
          <div class="md:col-span-2 flex items-center gap-3">
            <button type="submit" class="px-4 py-2 rounded-md brand-bg text-white">Send</button>
            <div id="contactMsg" class="text-sm text-gray-600"></div>
          </div>
        </form>
      </div>
    </section>

    <footer class="mt-12 text-center text-sm text-gray-500 pb-12">
      © <span id="year"></span> Jawad Ahmed — Designed & coded by you.
    </footer>
  </main>

  <!-- Project Modal (hidden by default) -->
  <div id="projModal" class="fixed inset-0 hidden items-center justify-center z-50">
    <div class="absolute inset-0 modal-backdrop" id="closeModal"></div>
    <div class="bg-white rounded-lg max-w-3xl w-full mx-4 overflow-y-auto max-h-[90vh] z-50 shadow-xl">
      <div class="flex items-start justify-between p-4 border-b">
        <div>
          <h4 id="modalTitle" class="text-lg font-semibold"></h4>
          <div id="modalCat" class="text-xs text-gray-500"></div>
        </div>
        <button id="closeBtn" class="p-2 text-gray-500 hover:text-gray-700">Close</button>
      </div>
      <div class="p-4 space-y-4">
        <div id="modalImages" class="grid grid-cols-1 sm:grid-cols-2 gap-3"></div>
        <p id="modalDesc" class="text-gray-700"></p>
      </div>
    </div>
  </div>

  <!-- Mobile menu overlay -->
  <div id="mobileMenu" class="fixed inset-0 z-40 hidden">
    <div class="absolute inset-0 modal-backdrop" id="mobileClose"></div>
    <div class="absolute right-0 top-0 bg-white w-64 h-full p-4 shadow-lg">
      <nav class="flex flex-col gap-3">
        <a href="#work" class="py-2">Work</a>
        <a href="#about" class="py-2">About</a>
        <a href="#contact" class="py-2">Contact</a>
        <a href="#" class="py-2 brand-bg text-white rounded inline-block text-center">Hire Me</a>
      </nav>
    </div>
  </div>

  <!-- Scripts -->
  <script>
    // basic helpers
    document.getElementById('year').textContent = new Date().getFullYear();

    // Portfolio filter
    const filters = document.querySelectorAll('.filterBtn');
    const cards = document.querySelectorAll('.projectCard');

    filters.forEach(btn => {
      btn.addEventListener('click', () => {
        filters.forEach(b => b.classList.remove('bg-gray-100','border'));
        btn.classList.add('bg-gray-100','border');
        const f = btn.dataset.filter;
        cards.forEach(c => {
          if (f === 'all' || c.dataset.cat === f) {
            c.style.display = '';
          } else {
            c.style.display = 'none';
          }
        });
      });
    });
    // set default active
    document.querySelector('.filterBtn[data-filter="all"]').classList.add('bg-gray-100','border');

    // Modal for project details
    const modal = document.getElementById('projModal');
    const modalTitle = document.getElementById('modalTitle');
    const modalCat = document.getElementById('modalCat');
    const modalDesc = document.getElementById('modalDesc');
    const modalImages = document.getElementById('modalImages');

    cards.forEach(card => {
      card.addEventListener('click', () => {
        modalTitle.textContent = card.dataset.title || 'Project';
        modalCat.textContent = card.dataset.cat || '';
        modalDesc.textContent = card.dataset.desc || '';
        modalImages.innerHTML = '';
        try {
          const imgs = JSON.parse(card.dataset.images || '[]');
          imgs.forEach(src => {
            const imgEl = document.createElement('img');
            imgEl.src = src;
            imgEl.className = 'w-full h-48 object-cover rounded';
            modalImages.appendChild(imgEl);
          });
        } catch (e) {
          // no images
        }
        modal.classList.remove('hidden');
        modal.classList.add('flex');
      });
    });

    document.getElementById('closeBtn').addEventListener('click', closeModal);
    document.getElementById('closeModal').addEventListener('click', closeModal);
    function closeModal() {
      modal.classList.add('hidden');
      modal.classList.remove('flex');
    }

    // Mobile menu toggle
    const mobileBtn = document.getElementById('mobileBtn');
    const mobileMenu = document.getElementById('mobileMenu');
    document.getElementById('mobileClose').addEventListener('click', () => mobileMenu.classList.add('hidden'));
    mobileBtn && mobileBtn.addEventListener('click', () => mobileMenu.classList.toggle('hidden'));

    // Contact form: simple mailto fallback
    const contactForm = document.getElementById('contactForm');
    const contactMsg = document.getElementById('contactMsg');
    contactForm.addEventListener('submit', function(e) {
      e.preventDefault();
      const form = new FormData(contactForm);
      const name = form.get('name');
      const email = form.get('email');
      const subject = form.get('subject') || 'Portfolio contact';
      const message = form.get('message');
      const body = encodeURIComponent(`Name: ${name}\nEmail: ${email}\n\n${message}`);
      // Open user's mail client
      window.location.href = `mailto:your-email@example.com?subject=${encodeURIComponent(subject)}&body=${body}`;
      contactMsg.textContent = "Opening your email client...";
      setTimeout(()=> contactMsg.textContent = "", 4000);
    });
  </script>
</body>
</html>

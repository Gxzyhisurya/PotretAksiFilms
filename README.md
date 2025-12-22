<!doctype html>
<html lang="id" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Potret Aksi Film</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&amp;family=Inter:wght@400;500;600;700&amp;display=swap" rel="stylesheet">
  <style>
    body {
      box-sizing: border-box;
    }
    .font-bebas {
      font-family: 'Bebas Neue', sans-serif;
    }
    .font-inter {
      font-family: 'Inter', sans-serif;
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full bg-black text-white font-inter">
  <div id="app" class="h-full w-full overflow-auto"><!-- Welcome Page -->
   <div id="welcome-page" class="min-h-full flex flex-col items-center justify-center px-6 py-12">
    <div class="text-center">
     <h1 id="main-title" class="font-inter text-4xl md:text-5xl font-semibold tracking-wide mb-4">POTRET AKSI FILM</h1>
     <div class="w-24 h-1 bg-white mx-auto mb-8"></div>
     <p class="text-gray-400 text-lg mb-12">Pesan tiket film favoritmu sekarang</p><button id="start-btn" class="bg-white text-black font-semibold px-8 py-4 text-lg hover:bg-gray-200 transition-colors duration-300"> Mulai Beli Tiket </button>
    </div>
   </div><!-- Movie List Page -->
   <div id="movie-page" class="min-h-full px-6 py-12 hidden">
    <div class="max-w-2xl mx-auto">
     <h2 id="site-title-header" class="font-inter text-2xl md:text-3xl font-semibold text-center mb-10 tracking-wide">POTRET AKSI FILM</h2><!-- Now Showing Section -->
     <div class="mb-12">
      <h3 class="text-xl font-semibold mb-6 text-white border-b border-gray-700 pb-2">NOW SHOWING</h3>
      <div class="space-y-4"><!-- Movie 1 -->
       <div class="movie-card bg-gray-900 p-5 border border-gray-800 cursor-pointer hover:border-gray-600 transition-colors" data-movie="searching">
        <h4 class="font-bebas text-2xl tracking-wide mb-2">SEARCHING FIRST CASE S01E01</h4>
        <div class="flex flex-wrap gap-3 text-sm"><span class="text-gray-400">Dokumenter, Thriller</span> <span class="bg-red-900 text-red-200 px-2 py-0.5">17+</span>
        </div>
       </div><!-- Movie 2 -->
       <div class="movie-card bg-gray-900 p-5 border border-gray-800 cursor-pointer hover:border-gray-600 transition-colors" data-movie="leuweung1">
        <h4 class="font-bebas text-2xl tracking-wide mb-2">LEUWEUNG SETAN 1</h4>
        <div class="flex flex-wrap gap-3 text-sm"><span class="text-gray-400">Horor, Drama</span> <span class="bg-red-900 text-red-200 px-2 py-0.5">17+</span>
        </div>
       </div>
      </div>
     </div><!-- Coming Soon Section -->
     <div>
      <h3 class="text-xl font-semibold mb-6 text-gray-300 border-b border-gray-700 pb-2">COMING SOON</h3>
      <div class="space-y-4"><!-- Coming Soon Movie -->
       <div class="bg-gray-900 p-5 border border-gray-800 opacity-70">
        <h4 class="font-bebas text-2xl tracking-wide mb-2 text-gray-300">LEUWEUNG SETAN 2</h4>
        <div class="flex flex-wrap gap-3 text-sm"><span class="text-gray-500">Horor, Thriller</span> <span class="bg-gray-800 text-gray-400 px-2 py-0.5">17+</span>
        </div>
        <p class="text-gray-500 text-sm mt-3">Segera Tayang</p>
       </div>
      </div>
     </div><button id="back-to-welcome" class="mt-10 text-gray-400 hover:text-white transition-colors"> Kembali </button>
    </div>
   </div><!-- Day Selection Page -->
   <div id="day-page" class="min-h-full px-6 py-12 hidden">
    <div class="max-w-2xl mx-auto">
     <h2 class="font-inter text-2xl md:text-3xl font-semibold text-center mb-4 tracking-wide">PILIH HARI</h2>
     <p id="selected-movie-for-day" class="text-center text-gray-400 mb-10"></p>
     <div class="space-y-3 mb-10"><button class="day-btn w-full bg-gray-900 border border-gray-700 py-4 text-lg font-semibold hover:bg-gray-800 hover:border-gray-500 transition-colors" data-day="Senin"> Senin </button> <button class="day-btn w-full bg-gray-900 border border-gray-700 py-4 text-lg font-semibold hover:bg-gray-800 hover:border-gray-500 transition-colors" data-day="Selasa"> Selasa </button> <button class="day-btn w-full bg-gray-900 border border-gray-700 py-4 text-lg font-semibold hover:bg-gray-800 hover:border-gray-500 transition-colors" data-day="Rabu"> Rabu </button> <button class="day-btn w-full bg-gray-900 border border-gray-700 py-4 text-lg font-semibold hover:bg-gray-800 hover:border-gray-500 transition-colors" data-day="Kamis"> Kamis </button> <button class="day-btn w-full bg-gray-900 border border-gray-700 py-4 text-lg font-semibold hover:bg-gray-800 hover:border-gray-500 transition-colors" data-day="Jumat"> Jumat </button>
     </div><button id="back-to-movies-from-day" class="text-gray-400 hover:text-white transition-colors"> Kembali ke Daftar Film </button>
    </div>
   </div><!-- Showtime Page -->
   <div id="showtime-page" class="min-h-full px-6 py-12 hidden">
    <div class="max-w-2xl mx-auto">
     <h2 class="font-inter text-2xl md:text-3xl font-semibold text-center mb-4 tracking-wide">PILIH JAM TAYANG</h2>
     <p id="selected-movie-title" class="text-center text-gray-400 mb-2"></p>
     <p id="selected-day-title" class="text-center text-gray-500 mb-10"></p>
     <div class="mb-8">
      <p class="text-gray-400 mb-4">Harga: <span class="text-white font-semibold">GRATIS</span></p>
     </div>
     <div class="grid grid-cols-3 gap-4 mb-10"><button class="showtime-btn bg-gray-900 border border-gray-700 py-4 text-lg font-semibold hover:bg-gray-800 hover:border-gray-500 transition-colors" data-time="11:00"> 11:00 </button> <button class="showtime-btn bg-gray-900 border border-gray-700 py-4 text-lg font-semibold hover:bg-gray-800 hover:border-gray-500 transition-colors" data-time="13:00"> 13:00 </button> <button class="showtime-btn bg-gray-900 border border-gray-700 py-4 text-lg font-semibold hover:bg-gray-800 hover:border-gray-500 transition-colors" data-time="14:55"> 14:55 </button>
     </div><button id="back-to-days" class="text-gray-400 hover:text-white transition-colors"> Kembali ke Pilih Hari </button>
    </div>
   </div><!-- Booking Confirmation Page -->
   <div id="confirmation-page" class="min-h-full px-6 py-12 hidden">
    <div class="max-w-2xl mx-auto text-center">
     <div class="mb-8">
      <div class="w-16 h-16 border-2 border-white mx-auto mb-6 flex items-center justify-center">
       <svg class="w-8 h-8" fill="none" stroke="currentColor" viewbox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
       </svg>
      </div>
      <h2 class="font-inter text-2xl md:text-3xl font-semibold tracking-wide mb-2">PEMESANAN BERHASIL</h2>
     </div>
     <div class="bg-gray-900 border border-gray-700 p-6 mb-6">
      <p class="text-gray-400 text-sm mb-2">Film</p>
      <p id="confirm-movie" class="font-bebas text-xl mb-4"></p>
      <p class="text-gray-400 text-sm mb-2">Hari</p>
      <p id="confirm-day" class="text-xl font-semibold mb-4"></p>
      <p class="text-gray-400 text-sm mb-2">Jam Tayang</p>
      <p id="confirm-time" class="text-xl font-semibold mb-4"></p>
      <p class="text-gray-400 text-sm mb-2">Kode Booking</p>
      <div class="bg-black border border-gray-600 p-4 mb-4">
       <p id="booking-code" class="font-bebas text-2xl tracking-widest"></p>
      </div><button id="copy-code-btn" class="bg-white text-black px-6 py-2 font-semibold hover:bg-gray-200 transition-colors"> Salin Kode </button>
      <p id="copy-feedback" class="text-green-400 text-sm mt-2 hidden">Kode berhasil disalin</p>
     </div>
     <div class="bg-gray-900 border border-gray-700 p-5 text-left">
      <p id="instagram-instruction" class="text-gray-300 leading-relaxed">Salin kode ini untuk nonton filmnya dan kirim DM di akun Instagram <span class="text-white font-semibold">Potretaksifilm</span></p>
     </div><button id="new-booking" class="mt-8 text-gray-400 hover:text-white transition-colors"> Pesan Tiket Lain </button>
    </div>
   </div>
  </div>
  <script>
    const defaultConfig = {
      site_title: 'POTRET AKSI FILM',
      instagram_account: 'Potretaksifilm',
      primary_color: '#ffffff',
      background_color: '#000000',
      surface_color: '#111827',
      text_color: '#ffffff',
      secondary_text_color: '#9ca3af',
      font_family: 'Inter',
      font_size: 16
    };

    let selectedMovie = null;
    let selectedDay = null;
    let selectedTime = null;

    const movies = {
      searching: 'SEARCHING FIRST CASE S01E01',
      leuweung1: 'LEUWEUNG SETAN 1'
    };

    function generateBookingCode() {
      const chars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789';
      let code = 'PAF-';
      for (let i = 0; i < 8; i++) {
        code += chars.charAt(Math.floor(Math.random() * chars.length));
      }
      return code;
    }

    function showPage(pageId) {
      document.querySelectorAll('#app > div').forEach(page => {
        page.classList.add('hidden');
      });
      document.getElementById(pageId).classList.remove('hidden');
    }

    // Navigation Events
    document.getElementById('start-btn').addEventListener('click', () => {
      showPage('movie-page');
    });

    document.getElementById('back-to-welcome').addEventListener('click', () => {
      showPage('welcome-page');
    });

    

    document.getElementById('new-booking').addEventListener('click', () => {
      showPage('movie-page');
    });

    // Movie Selection
    document.querySelectorAll('.movie-card').forEach(card => {
      card.addEventListener('click', () => {
        selectedMovie = card.dataset.movie;
        document.getElementById('selected-movie-for-day').textContent = movies[selectedMovie];
        showPage('day-page');
      });
    });

    // Back from day page
    document.getElementById('back-to-movies-from-day').addEventListener('click', () => {
      showPage('movie-page');
    });

    // Day Selection
    document.querySelectorAll('.day-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        selectedDay = btn.dataset.day;
        document.getElementById('selected-movie-title').textContent = movies[selectedMovie];
        document.getElementById('selected-day-title').textContent = 'Hari: ' + selectedDay;
        showPage('showtime-page');
      });
    });

    // Back to day selection
    document.getElementById('back-to-days').addEventListener('click', () => {
      showPage('day-page');
    });

    // Showtime Selection
    document.querySelectorAll('.showtime-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        selectedTime = btn.dataset.time;
        document.getElementById('confirm-movie').textContent = movies[selectedMovie];
        document.getElementById('confirm-day').textContent = selectedDay;
        document.getElementById('confirm-time').textContent = selectedTime;
        document.getElementById('booking-code').textContent = generateBookingCode();
        document.getElementById('copy-feedback').classList.add('hidden');
        showPage('confirmation-page');
      });
    });

    // Copy Code
    document.getElementById('copy-code-btn').addEventListener('click', () => {
      const code = document.getElementById('booking-code').textContent;
      navigator.clipboard.writeText(code).then(() => {
        document.getElementById('copy-feedback').classList.remove('hidden');
        setTimeout(() => {
          document.getElementById('copy-feedback').classList.add('hidden');
        }, 2000);
      });
    });

    // Element SDK Integration
    async function onConfigChange(config) {
      const siteTitle = config.site_title || defaultConfig.site_title;
      const instagramAccount = config.instagram_account || defaultConfig.instagram_account;
      const fontFamily = config.font_family || defaultConfig.font_family;
      const fontSize = config.font_size || defaultConfig.font_size;

      document.getElementById('main-title').textContent = siteTitle;
      document.getElementById('site-title-header').textContent = siteTitle;
      
      document.getElementById('instagram-instruction').innerHTML = 
        `Salin kode ini untuk nonton filmnya dan kirim DM di akun Instagram <span class="text-white font-semibold">${instagramAccount}</span>`;

      document.body.style.fontFamily = `${fontFamily}, Inter, sans-serif`;
      document.querySelectorAll('.font-bebas').forEach(el => {
        el.style.fontFamily = `Bebas Neue, ${fontFamily}, sans-serif`;
      });

      document.body.style.fontSize = `${fontSize}px`;
    }

    function mapToCapabilities(config) {
      return {
        recolorables: [],
        borderables: [],
        fontEditable: {
          get: () => config.font_family || defaultConfig.font_family,
          set: (value) => {
            config.font_family = value;
            window.elementSdk.setConfig({ font_family: value });
          }
        },
        fontSizeable: {
          get: () => config.font_size || defaultConfig.font_size,
          set: (value) => {
            config.font_size = value;
            window.elementSdk.setConfig({ font_size: value });
          }
        }
      };
    }

    function mapToEditPanelValues(config) {
      return new Map([
        ['site_title', config.site_title || defaultConfig.site_title],
        ['instagram_account', config.instagram_account || defaultConfig.instagram_account]
      ]);
    }

    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange,
        mapToCapabilities,
        mapToEditPanelValues
      });
    }
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9b1fbfc860888de9',t:'MTc2NjQwNzg3MS4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>

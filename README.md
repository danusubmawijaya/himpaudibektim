
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover, maximum-scale=5.0, user-scalable=yes">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <meta name="apple-mobile-web-app-title" content="HIMPAUDI">
  <meta name="theme-color" content="#1E56A0">
  <title>Beranda - HIMPAUDI Bekasi Timur</title>

  <link rel="stylesheet" href="/himpaudi-bekasi-timur/public/assets/css/style.css?v=1793107123">
  <link rel="stylesheet" href="/himpaudi-bekasi-timur/public/assets/css/navbar-fix.css?v=1793107123">
  <link rel="stylesheet" href="/himpaudi-bekasi-timur/public/assets/css/mobile-fix-complete.css?v=1793107123">
  <link rel="stylesheet" href="/himpaudi-bekasi-timur/public/assets/css/dropdown-fix.css?v=1793107123">
  <link rel="stylesheet" href="/himpaudi-bekasi-timur/public/assets/css/back-to-top.css?v=1793107123">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

  <style>
    :root {
      --vh: 1vh;
      --safe-top: env(safe-area-inset-top, 0px);
      --safe-bottom: env(safe-area-inset-bottom, 0px);
    }

    body {
      padding-top: 64px;
      overflow-x: hidden;
    }

    .navbar{
      position:fixed;
      top:0;
      left:0;
      right:0;
      z-index:1000;
      background:#ffffff;
      transition:box-shadow .25s ease, transform .3s ease;
      border-bottom:1px solid rgba(30,86,160,0.08);
      padding-top: var(--safe-top);
      width: 100%;
      overflow: hidden;
      max-width: 100%;
      height: auto;
      max-height: 100vh;
    }
    .navbar.navbar-shadow{ box-shadow:0 10px 24px rgba(20,40,80,0.08); }
    .navbar .container{
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:16px;
      padding:14px 16px;
      max-width:100%;
      margin:0 auto;
      width: 100%;
      box-sizing: border-box;
      overflow: hidden;
    }
    .navbar .logo{ display:flex; align-items:center; gap:12px; }
    .navbar .logo img{ width:48px; height:48px; object-fit:cover; }
    .navbar .logo-text h1{ margin:0; font-size:18px; font-weight:700; color:#1E56A0; }
    .navbar .logo-text p{ margin:0; font-size:12px; color:#6b7280; }

    .nav-toggle{
      display:none;
      flex-direction:column;
      gap:5px;
      background:transparent;
      border:none;
      cursor:pointer;
      padding:8px;
      -webkit-appearance: none;
      appearance: none;
      z-index: 1001;
      position: relative;
      min-width: 44px;
      min-height: 44px;
    }
    .nav-toggle span{
      width:24px;
      height:2px;
      background:#1E56A0;
      border-radius:2px;
      transition:transform .25s ease, opacity .25s ease;
    }

    .nav-menu{
      display:flex;
      align-items:center;
      gap:16px;
      z-index: 999;
      overflow: hidden;
      max-width: 100%;
      flex-wrap: nowrap;
    }
    .nav-link{
      position:relative;
      font-weight:600;
      font-size:14px;
      color:#1E56A0;
      text-decoration:none;
      padding:6px 10px;
      border-radius:8px;
      transition:all .25s ease;
      -webkit-tap-highlight-color: transparent;
      white-space: nowrap;
      flex-shrink: 0;
    }
    .nav-link:hover{ 
      background: rgba(30,86,160,0.06);
    }
    .nav-link.active{
      background: linear-gradient(90deg, #ffd54f, #ff9800);
      color: #111;
      font-weight: 700;
      box-shadow: 0 2px 8px rgba(255, 152, 0, 0.3);
      transform: translateY(-1px);
    }
    .nav-link.active:hover{
      filter: brightness(1.08);
    }
    
    .btn-login{
      padding:8px 14px;
      border-radius:999px;
      border:1px solid transparent;
      color:#ffffff;
      background:linear-gradient(120deg,#1E56A0,#3f7bd2);
      font-weight:600;
      display:inline-flex;
      align-items:center;
      gap:6px;
      transition:all .25s ease;
      -webkit-tap-highlight-color: transparent;
      cursor: pointer;
      white-space: nowrap;
      font-size: 13px;
      flex-shrink: 0;
    }
    .btn-login:hover{ 
      filter:brightness(1.05);
      transform: translateY(-1px);
    }
    .btn-login.active{
      background: linear-gradient(90deg, #ffd54f, #ff9800);
      color: #111;
      box-shadow: 0 2px 8px rgba(255, 152, 0, 0.3);
    }

    @media (max-width: 960px) {
      .navbar .container {
        padding: 12px 16px;
        width: 100%;
        box-sizing: border-box;
        overflow-x: hidden;
      }

      .nav-toggle {
        display: flex !important;
        z-index: 1001;
      }

      .nav-menu {
        position: fixed;
        top: 64px;
        left: 0;
        right: 0;
        width: 100%;
        background: #ffffff;
        flex-direction: column;
        align-items: stretch;
        gap: 0;
        padding: 0;
        border-bottom: 1px solid rgba(30, 86, 160, 0.08);
        max-height: 0;
        overflow: hidden;
        transition: max-height 0.3s ease;
        z-index: 999;
        box-sizing: border-box;
      }

      .nav-menu.open {
        max-height: calc(100vh - 64px);
        padding: 0;
      }

      .nav-link {
        width: 100%;
        padding: 14px 16px;
        border-bottom: 1px solid #f0f0f0;
        display: block;
        box-sizing: border-box;
      }

      .nav-menu .btn-login {
        width: calc(100% - 32px);
        margin: 12px 16px;
        padding: 12px 16px;
        text-align: center;
        box-sizing: border-box;
      }
    }
  </style>
</head>
<body>

<!-- ===== NAVBAR ===== -->
<header class="navbar">
  <div class="container">
    <div class="logo">
      <img src="/himpaudi-bekasi-timur/public/assets/img/LOGOHIMPAUDI.png" alt="Logo HIMPAUDI">
      <div class="logo-text">
        <h1>HIMPAUDI</h1>
        <p>Bekasi Timur</p>
      </div>
    </div>

    <button class="nav-toggle" aria-label="Toggle navigation">
      <span></span>
      <span></span>
      <span></span>
    </button>

    <nav class="nav-menu">
      <a href="/himpaudi-bekasi-timur/public/index.php" class="nav-link active">Beranda</a>
      
      <div class="nav-dropdown" id="profilDropdown">
        <div class="nav-link dropdown-toggle">
          Profil <i class="fa-solid fa-chevron-down"></i>
        </div>
        <div class="dropdown-content">
          <a href="/himpaudi-bekasi-timur/public/profil/visi-misi.php">Visi & Misi</a>
          <a href="/himpaudi-bekasi-timur/public/profil/tujuan.php">Tujuan</a>
          <a href="/himpaudi-bekasi-timur/public/profil/struktur-organisasi.php">Struktur Organisasi</a>
        </div>
      </div>
       <a href="/himpaudi-bekasi-timur/public/lembaga_paud.php#data_lembaga" class="nav-link ">Data Lembaga</a>
      <a href="/himpaudi-bekasi-timur/public/index.php#berita" class="nav-link">Berita</a>
      <a href="/himpaudi-bekasi-timur/public/index.php#galeri" class="nav-link">Galeri</a>
      <a href="/himpaudi-bekasi-timur/public/index.php#kontak" class="nav-link">Kontak</a>
      <a href="/himpaudi-bekasi-timur/public/faq.php" class="nav-link ">F.A.Q</a>

                        <a href="/himpaudi-bekasi-timur/public/register.php" class="btn-login nav-link " data-page="register.php">Masuk</a>
                  </nav>
  </div>
</header>

<script src="/himpaudi-bekasi-timur/public/assets/js/mobile-responsive.js?v=1793107123"></script>
<script src="/himpaudi-bekasi-timur/public/assets/js/back-to-top.js?v=1793107123"></script>

</body>
</html>
<div id="main-content">
<!-- ===== HERO SECTION ===== -->
<section class="hero">
  <div class="hero-container">
    <div class="hero-text">
      <h1>Selamat Datang di Website<br>HIMPAUDI Kecamatan Bekasi Timur</h1>
      <p>
        Menginspirasi dan memberdayakan para pendidik anak usia dini untuk menciptakan
        pembelajaran yang berkualitas, berlandaskan nilai-nilai moral, sosial, dan kebangsaan.
      </p>
      <div class="btn-wrapper">
        <a href="/himpaudi-bekasi-timur/public/panduan.php" class="btn-secondary">Panduan</a>
        <a href="https://himpaudi.org/register/" class="btn-primary">Daftar Keanggotaan</a>
        <i class="fa-solid fa-arrow-right arrow-icon"></i>
      </div>
    </div>
    <div class="hero-image">
      <img src="/himpaudi-bekasi-timur/public/assets/img/LOGOHIMPAUDI.png" alt="Ilustrasi HIMPAUDI">
    </div>
  </div>
</section>

<!-- ===== TENTANG KAMI ===== -->
<section class="about" id="tentang">
  <h2 class="about-title">Tentang Kami</h2>
  <div class="about-container">
    <div class="about-image">
      <img src="/himpaudi-bekasi-timur/public/assets/img/about1.png" alt="Kegiatan HIMPAUDI">
    </div>
    <div class="about-text">
      <h3>Himpunan Pendidik dan Tenaga Kependidikan Anak Usia Dini Indonesia</h3>
      <p>
        <strong>HIMPAUDI Kecamatan Bekasi Timur</strong> adalah organisasi profesi yang mewadahi para pendidik dan tenaga kependidikan anak usia dini di wilayah Kecamatan Bekasi Timur. 
        Kami berkomitmen untuk meningkatkan kualitas pendidikan anak usia dini melalui berbagai program pelatihan, pendampingan, dan kegiatan kolaboratif.
      </p>
      <p>
        Dengan lebih dari <strong>38</strong> lembaga PAUD yang tergabung, kami terus berinovasi dan berkembang untuk memberikan layanan terbaik bagi pendidikan anak-anak Indonesia.
      </p>
      <a href="/himpaudi-bekasi-timur/public/tentang.php" class="btn-secondary">Selengkapnya</a>
      <i class="fa-solid fa-arrow-right arrow-icon"></i>
    </div>
  </div>
</section>

<!-- ===== STATISTIK ===== -->
<section class="stats" id="statistik">
  <div class="stats-grid">
    <div class="stat-card">
      <i class="fa-solid fa-school"></i>
      <h3>38</h3>
      <p>Lembaga PAUD</p>
    </div>

    <div class="stat-card">
      <i class="fa-solid fa-chalkboard-user"></i>
      <h3>184</h3>
      <p>Guru & Tenaga Kependidikan</p>
    </div>

    <div class="stat-card">
      <i class="fa-solid fa-calendar-days"></i>
      <h3>3</h3>
      <p>Kegiatan Terprogram</p>
    </div>

    <div class="stat-card">
      <i class="fa-solid fa-users-viewfinder"></i>
      <h3>4</h3>
      <p>Total Pengunjung</p>
    </div>
  </div>
</section>

<!-- ===== BERITA & KEGIATAN ===== -->
<section class="news" id="berita">
  <div class="news-container">
    <h2>Berita & Kegiatan Terbaru</h2>
    <p class="news-subtitle">Informasi terkini dari HIMPAUDI Bekasi Timur</p>
    
    <div class="news-grid">
              <div class="news-item">
          <div class="news-item-image">
            <img src="https://picsum.photos/seed/news10/400/250" 
                 alt="testing berita ">
                          <span class="news-badge berita-badge">Berita</span>
                      </div>
          <div class="news-content">
            <div class="news-meta">
              <span class="news-date">
                <i class="fa-regular fa-calendar"></i>
                15 Jan 2026              </span>
            </div>
            <h4>testing berita </h4>
            <p class="news-excerpt">3...</p>
                        <a href="/himpaudi-bekasi-timur/public/berita_detail.php?id=10" class="news-link">
              Selengkapnya <i class="fa-solid fa-arrow-right"></i>
            </a>
          </div>
        </div>
              <div class="news-item">
          <div class="news-item-image">
            <img src="/himpaudi-bekasi-timur/public/uploads/berita/berita_1763611560_691e93a86277a.png" 
                 alt="te">
                          <span class="news-badge berita-badge">Berita</span>
                      </div>
          <div class="news-content">
            <div class="news-meta">
              <span class="news-date">
                <i class="fa-regular fa-calendar"></i>
                20 Nov 2025              </span>
            </div>
            <h4>te</h4>
            <p class="news-excerpt">tttt...</p>
                        <a href="/himpaudi-bekasi-timur/public/berita_detail.php?id=7" class="news-link">
              Selengkapnya <i class="fa-solid fa-arrow-right"></i>
            </a>
          </div>
        </div>
              <div class="news-item">
          <div class="news-item-image">
            <img src="/himpaudi-bekasi-timur/public/uploads/berita/berita_1763215324.jpg" 
                 alt="Penguatan Motivasi Guru Bekasi untuk Tingkatkan Kompetensi dan Kolaborasi">
                          <span class="news-badge berita-badge">Berita</span>
                      </div>
          <div class="news-content">
            <div class="news-meta">
              <span class="news-date">
                <i class="fa-regular fa-calendar"></i>
                15 Nov 2025              </span>
            </div>
            <h4>Penguatan Motivasi Guru Bekasi untuk Tingkatkan Kompetensi dan Kolaborasi</h4>
            <p class="news-excerpt">Kegiatan ini diselenggarakan sebagai upaya mendorong para guru di Kota Bekasi untuk terus ...</p>
                        <a href="/himpaudi-bekasi-timur/public/berita_detail.php?id=6" class="news-link">
              Selengkapnya <i class="fa-solid fa-arrow-right"></i>
            </a>
          </div>
        </div>
          </div>

    <div class="news-button">
      <a href="/himpaudi-bekasi-timur/public/berita-semua.php" class="btn-news">Lihat Semua Berita <i class="fa-solid fa-arrow-right"></i></a>
    </div>
  </div>
</section>

<!-- ===== GALERI ===== -->
<section class="gallery" id="galeri">
  <h2>Galeri Kegiatan</h2>
  <div class="gallery-grid">
                  <img src="/himpaudi-bekasi-timur/public/uploads/gallery/696f3618a7f35_1768896024.jpg" 
             alt="TES">
              <img src="/himpaudi-bekasi-timur/public/uploads/gallery/6964ab19c820b_1768205081.jpg" 
             alt="Pembinaan Guru PAUD tentang SPMI">
              <img src="/himpaudi-bekasi-timur/public/uploads/gallery/6964a2a1b0667_1768202913.jpg" 
             alt="Workshop">
              <img src="/himpaudi-bekasi-timur/public/uploads/gallery/691d7da4303ed_1763540388.jpg" 
             alt="tes 1 galeri">
            </div>
  <a href="/himpaudi-bekasi-timur/public/galeri.php" class="btn-secondary">Lihat Semua Galeri</a>
</section>

<!-- ===== HUBUNGI KAMI ===== -->
<section class="contact" id="kontak">
  <h2>Hubungi Kami</h2>
  <p class="contact-subtitle">Kami siap membantu dan menjawab pertanyaan Anda</p>

  <div class="contact-wrapper">
    <!-- Info Kontak -->
    <div class="contact-info-box">
      <h3>Informasi Kontak</h3>
      <div class="contact-item">
        <img src="/himpaudi-bekasi-timur/public/assets/icons/mdi_location.png" alt="Alamat">
        <div>
          <h4>Alamat</h4>
          <p>jl kusuma selatan raya, RT 009 RW 019 kel. aren jaya, .Bekasi Timur</p>
        </div>
      </div>

      <div class="contact-item">
        <img src="/himpaudi-bekasi-timur/public/assets/icons/mynaui_telephone-solid.png" alt="Telepon">
        <div>
          <h4>Telepon</h4>
          <p>0812-9064-0416</p>
        </div>
      </div>

      <div class="contact-item">
        <img src="/himpaudi-bekasi-timur/public/assets/icons/mynaui_telephone-solid.png" alt="Telepon">
        <div>
          <h4>Telepon</h4>
          <p>0858-1457-5189</p>
        </div>
      </div>

      <div class="contact-item">
        <img src="/himpaudi-bekasi-timur/public/assets/icons/uiw_mail.png" alt="Email">
        <div>
          <h4>Email</h4>
          <p>himpaudibektim01@gmail.com</p>
        </div>
      </div>

      <div class="contact-item">
        <img src="/himpaudi-bekasi-timur/public/assets/icons/mdi_clock.png" alt="Jam Operasional">
        <div>
          <h4>Jam Operasional</h4>
          <p>Senin - Jumat: 08.00 - 17.00<br>Sabtu: 09.00 - 14.00</p>
        </div>
      </div>

      <div class="socials">
        <p>Ikuti Kami</p>
        <a href="https://facebook.com/himpaudi.bekasitimur" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
        <a href="https://instagram.com/himpaudi_bekasitimur" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
      </div>
    </div>

    <!-- Form Kirim Pesan -->
    <div class="contact-form-box">
      <h3>Kirim Pesan</h3>
      <form id="contactForm" method="GET" action="mailto:himpaudibektim01@gmail.com">
        <label>Nama Lengkap</label>
        <input type="text" id="nama" placeholder="Nama lengkap anda" required>

        <div class="form-row">
          <div class="form-group">
            <label>Email</label>
            <input type="email" id="email" placeholder="emailanda@gmail.com" required>
          </div>
          <div class="form-group">
            <label>Nomor Telepon</label>
            <input type="text" id="telepon" placeholder="08xxxxxxxx" maxlength="16" inputmode="numeric" required>
          </div>
        </div>

        <label>Subjek Pesan</label>
        <input type="text" id="subject" placeholder="Subjek Pesan" required>

        <label>Pesan</label>
        <textarea id="pesan" placeholder="Tulis pesan anda disini..." required></textarea>

        <button type="submit" class="btn-primary" id="submitBtn">
         <i class="fa-solid fa-paper-plane"></i> Kirim Pesan
        </button>
        
        <p class="contact-note">
          <i class="fa-solid fa-info-circle"></i> Pesan akan dibuka melalui aplikasi email Anda.
        </p>
      </form>
    </div>
  </div>
</section>

<!-- ===== LINK PENTING ===== -->
<section class="important-links" id="link-penting">
  <div class="important-links-container">
    <h2>Link Penting & Referensi</h2>
    
    <div class="links-grid">
      <!-- HIMPAUDI Pusat -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-globe"></i>
        </div>
        <div class="link-card-content">
          <h3>HIMPAUDI Pusat</h3>
          <p>Kunjungi website resmi HIMPAUDI Pusat untuk informasi lengkap organisasi.</p>
          <a href="https://www.himpaudi.org" target="_blank" rel="noopener noreferrer">
            Kunjungi <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>

      <!-- Portal Dapodik -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-database"></i>
        </div>
        <div class="link-card-content">
          <h3>Portal Dapodik</h3>
          <p>Sistem data pokok pendidikan untuk manajemen data sekolah dan guru.</p>
          <a href="https://dapo.kemendikdasmen.go.id" target="_blank" rel="noopener noreferrer">
            Akses <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>

      <!-- Manajemen Sekolah -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-school"></i>
        </div>
        <div class="link-card-content">
          <h3>Manajemen Sekolah</h3>
          <p>Platform untuk manajemen data sekolah dan administrasi pendidikan.</p>
          <a href="https://sp.datadik.kemendikdasmen.go.id" target="_blank" rel="noopener noreferrer">
            Akses <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>

      <!-- Individual GTK -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-user-tie"></i>
        </div>
        <div class="link-card-content">
          <h3>Individual GTK</h3>
          <p>Data individu Guru dan Tenaga Kependidikan untuk verifikasi dan validasi.</p>
          <a href="https://ptk.datadik.dikdasmen.go.id" target="_blank" rel="noopener noreferrer">
            Akses <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>

      <!-- BOS Online -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-money-bill-wave"></i>
        </div>
        <div class="link-card-content">
          <h3>BOS Online</h3>
          <p>Sistem pengelolaan Dana Bantuan Operasional Sekolah secara online.</p>
          <a href="http://bos.kemendikdasmen.go.id" target="_blank" rel="noopener noreferrer">
            Akses <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>

      <!-- Verval SP -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-check-circle"></i>
        </div>
        <div class="link-card-content">
          <h3>Verval SP</h3>
          <p>Verifikasi dan validasi data Satuan Pendidikan untuk akurasi data.</p>
          <a href="http://vervalsp.data.kemendikdasmen.go.id" target="_blank" rel="noopener noreferrer">
            Akses <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>

      <!-- Verval PTK -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-id-card"></i>
        </div>
        <div class="link-card-content">
          <h3>Verval PTK</h3>
          <p>Verifikasi dan validasi data Pendidik dan Tenaga Kependidikan.</p>
          <a href="http://vervalptk.data.kemendikdasmen.go.id" target="_blank" rel="noopener noreferrer">
            Akses <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>

      <!-- Verval PD -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-graduation-cap"></i>
        </div>
        <div class="link-card-content">
          <h3>Verval PD</h3>
          <p>Verifikasi dan validasi data Peserta Didik untuk kelengkapan data.</p>
          <a href="http://vervalpd.data.kemendikdasmen.go.id" target="_blank" rel="noopener noreferrer">
            Akses <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>

      <!-- Keaktifan NUPTK -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-badge-check"></i>
        </div>
        <div class="link-card-content">
          <h3>Keaktifan NUPTK</h3>
          <p>Cek status keaktifan Nomor Unik Pendidik dan Tenaga Kependidikan.</p>
          <a href="http://gtk.data.kemendikdasmen.go.id" target="_blank" rel="noopener noreferrer">
            Akses <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>

      <!-- Sekolah Kita -->
      <div class="link-card">
        <div class="link-card-icon">
          <i class="fa-solid fa-building"></i>
        </div>
        <div class="link-card-content">
          <h3>Sekolah Kita</h3>
          <p>Platform informasi publik tentang data sekolah dan kinerja pendidikan.</p>
          <a href="http://sekolah.data.kemendikdasmen.go.id" target="_blank" rel="noopener noreferrer">
            Akses <i class="fa-solid fa-arrow-right"></i>
          </a>
        </div>
      </div>
    </div>

    <!-- Social Links -->
    <div class="social-links">
      <a href="https://instagram.com/ditjen.paud.dikdasmen" target="_blank" rel="noopener noreferrer" class="social-link" title="IG Ditjen Paud Dikdasmen">
        <i class="fab fa-instagram"></i>
      </a>
      <a href="https://instagram.com/dapodik_official" target="_blank" rel="noopener noreferrer" class="social-link" title="IG Dapodik">
        <i class="fab fa-instagram"></i>
      </a>
    </div>
  </div>
</section>

<!-- ===== PETA ===== -->
<section class="map" id="peta">
  <h2>Lokasi Kami</h2>
  <div class="map-container">
    <iframe src="https://www.google.com/maps?q=Jl%20Kusuma%20Selatan%20Raya%2C%20RT%20009%20RW%20019%2C%20Aren%20Jaya%2C%20Bekasi%20Timur&output=embed" width="100%" height="400" style="border:0; border-radius: 10px; box-shadow: 0 4px 10px rgba(0,0,0,0.15);" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
  </div>
</section>
</div>

<!-- ===== FOOTER ===== -->
<footer class="footer">
  <div class="footer-wrapper">
    <div class="footer-container">
      <!-- Kolom 1 -->
      <div class="footer-about">
        <h3>HIMPAUDI Bekasi Timur</h3>
        <p>
          Himpunan Pendidik dan Tenaga Kependidikan Anak Usia Dini Indonesia Kecamatan Bekasi Timur.
        </p>
      </div>

      <!-- Kolom 2 -->
      <div class="footer-contact">
        <h4>Kontak Kami</h4>
        <p><i class="fa-solid fa-location-dot"></i> Jl Kusuma Selatan Raya, RT 009 RW 019 Kel. Aren Jaya, Kec. Bekasi Timur</p>
        <p><i class="fa-solid fa-phone"></i> 0812-9064-0416</p>
        <p><i class="fa-solid fa-phone"></i> 0858-1457-5189</p>
        <p><i class="fa-solid fa-envelope"></i> himpaudibektim01@gmail.com</p>
      </div>

      <!-- Kolom 3 -->
      <div class="footer-social">
        <h4>Ikuti Kami</h4>
        <div class="footer-socials">
          <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
          <a href="https://www.instagram.com/himpaudi.bektim?igsh=emU5Ym9pdmxhc3lh" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
        </div>
      </div>
    </div>

    <div class="footer-bottom">
      <p>Copyright &copy; 2026 HIMPAUDI (DANU) Kecamatan Bekasi Timur. Semua Hak Dilindungi.</p>
    </div>
  </div>
</footer>

<style>
/* Footer Base Styles */
footer.footer {
  background-color: #1a1a1a;
  color: #ffffff;
  padding: 40px 0 20px;
  margin-top: 60px;
  font-size: 14px;
  line-height: 1.6;
  width: 100%;
  overflow: hidden;
}

/* Wrapper = full layar */
.footer-wrapper {
  width: 100%;
}

/* Container = full width */
.footer-container {
  width: 100%;
  max-width: 1180px;
  margin: 0 auto 50px auto;
  padding: 0 12px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
  box-sizing: border-box;
}




.footer-about,
.footer-contact,
.footer-social {
  min-width: 0;
}

.footer-about h3,
.footer-contact h4,
.footer-social h4 {
  margin: 0 0 15px 0;
  font-size: 16px;
  font-weight: 600;
}

.footer-about p {
  margin: 0;
  font-size: 13px;
  line-height: 1.5;
}

.footer-contact p {
  margin: 8px 0;
  font-size: 13px;
  display: flex;
  align-items: flex-start;
  gap: 10px;
}

.footer-contact i {
  min-width: 16px;
  margin-top: 2px;
}

.footer-socials {
  display: flex;
  gap: 15px;
  margin-top: 10px;
}

.footer-socials a {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background-color: rgba(255, 255, 255, 0.1);
  color: #ffffff;
  border-radius: 50%;
  text-decoration: none;
  transition: background-color 0.3s ease;
  font-size: 18px;
}

.footer-socials a:hover {
  background-color: rgba(255, 255, 255, 0.2);
}

.footer-bottom {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  padding: 20px 12px;
  text-align: center;
  font-size: 12px;
  color: rgba(255, 255, 255, 0.7);
  max-width: 1180px;
  margin: 0 auto;
}
/* Tablet (768px and below) */
@media (max-width: 768px) {
  footer.footer {
    padding: 30px 0 15px 0;
    margin-top: 40px;
  }

  .footer-wrapper {
    padding: 0;
  }

  .footer-container {
    grid-template-columns: 1fr;
    gap: 25px;
    margin-bottom: 20px;
    padding: 0 20px;
    width: 100%;
    max-width: 100%;
  }

  .footer-about h3,
  .footer-contact h4,
  .footer-social h4 {
    font-size: 15px;
  }

  .footer-about p,
  .footer-contact p {
    font-size: 12px;
  }
}

/* Mobile (480px and below) */
@media (max-width: 480px) {
  footer.footer {
    padding: 25px 0 15px 0;
    margin-top: 30px;
    font-size: 13px;
  }

  .footer-wrapper {
    padding: 0;
  }

  .footer-container {
    grid-template-columns: 1fr;
    gap: 20px;
    margin-bottom: 15px;
    padding: 0 15px;
    width: 100%;
    max-width: 100%;
  }

  .footer-about h3,
  .footer-contact h4,
  .footer-social h4 {
    font-size: 14px;
    margin-bottom: 10px;
  }

  .footer-about p,
  .footer-contact p {
    font-size: 11px;
    margin: 6px 0;
  }

  .footer-contact p {
    gap: 8px;
  }

  .footer-socials {
    gap: 12px;
  }

  .footer-socials a {
    width: 36px;
    height: 36px;
    font-size: 16px;
  }

  .footer-bottom {
    padding-top: 15px;
    font-size: 11px;
  }
}

/* Extra Small (320px and below) */
@media (max-width: 320px) {
  footer.footer {
    padding: 20px 0 12px 0;
    margin-top: 25px;
  }

  .footer-wrapper {
    padding: 0;
  }

  .footer-container {
    gap: 15px;
    padding: 0 12px;
    width: 100%;
    max-width: 100%;
  }

  .footer-about h3,
  .footer-contact h4,
  .footer-social h4 {
    font-size: 13px;
    margin-bottom: 8px;
  }

  .footer-about p,
  .footer-contact p {
    font-size: 10px;
    margin: 5px 0;
  }

  .footer-socials a {
    width: 32px;
    height: 32px;
    font-size: 14px;
  }
}
</style>

<!-- efek shadow navbar -->
<script>
window.addEventListener('scroll', function() {
  const navbar = document.querySelector('.navbar');
  navbar.classList.toggle('scrolled', window.scrollY > 20);
});
</script>

<!-- Font Awesome buat ikon -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

</body>
</html>

<!-- Important Links CSS -->
<link rel="stylesheet" href="/himpaudi-bekasi-timur/public/assets/css/important-links.css">

<!-- Index Mobile Cards CSS (4 card per baris di mobile) -->
<link rel="stylesheet" href="/himpaudi-bekasi-timur/public/assets/css/index-mobile-cards.css">

<!-- Bubble Chat CSS & JS -->
<link rel="stylesheet" href="/himpaudi-bekasi-timur/public/assets/css/bubble-chat.css">
<script src="/himpaudi-bekasi-timur/public/assets/js/bubble-chat.js"></script>

<script>
// Handle Contact Form Submission dengan mailto
document.getElementById('contactForm').addEventListener('submit', function(e) {
    e.preventDefault();

    const nama = document.getElementById('nama').value.trim();
    const email = document.getElementById('email').value.trim();
    const telepon = document.getElementById('telepon').value.trim();
    const subject = document.getElementById('subject').value.trim();
    const pesan = document.getElementById('pesan').value.trim();

    // Validasi input
    if (!nama || !email || !telepon || !subject || !pesan) {
        alert('Mohon isi semua field yang diperlukan');
        return;
    }

    // Validasi nomor telepon (hanya angka, maksimal 16 digit)
    if (!/^\d+$/.test(telepon)) {
        alert('Nomor telepon hanya boleh berisi angka');
        return;
    }

    if (telepon.length > 16) {
        alert('Nomor telepon maksimal 16 digit');
        return;
    }

    // Format body email dengan line break
    const bodyText = `Nama Lengkap: ${nama}%0AEmail: ${email}%0ANomor Telepon: ${telepon}%0A%0AIsi Pesan:%0A${pesan}`;

    // Buat mailto link
    const mailtoLink = `mailto:himpaudibektim01@gmail.com?subject=${encodeURIComponent(subject)}&body=${bodyText}`;

    // Buka aplikasi email
    window.location.href = mailtoLink;

    // Reset form setelah beberapa saat
    setTimeout(() => {
        document.getElementById('contactForm').reset();
    }, 500);
});

// Validasi input telepon real-time - hanya angka
document.getElementById('telepon').addEventListener('input', function(e) {
    this.value = this.value.replace(/[^\d]/g, '');
});
</script>

<style>
.contact-note {
    font-size: 13px;
    color: #666;
    margin-top: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
}

.contact-note i {
    color: #0066cc;
    font-size: 14px;
}
</style>

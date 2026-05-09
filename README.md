<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Madham Rajeshwari Complex - Ahobilam</title>
    <!-- CSS లింక్ -->
    <link rel="stylesheet" href="style.css">
    <!-- ఫాంట్స్ కోసం Google Fonts లింక్ -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">
    <!-- ఐకాన్స్ కోసం FontAwesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

    <style>
        /* --- జూమ్ మరియు గ్యాప్ సమస్యల కోసం పరిష్కారం --- */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body, html {
            overflow-x: hidden; /* ఎడమ వైపు గ్రే గ్యాప్ రాకుండా ఆపుతుంది */
            width: 100%;
            background-color: #000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%; /* కంటెంట్ సెంటర్ లో ఉండటానికి */
            background-color: #111;
            position: sticky;
            top: 0;
            z-index: 1000;
            width: 100%;
            border-bottom: 1px solid #333;
        }

        .right-section {
            display: flex !important;
            align-items: center;
            gap: 15px;
            min-width: max-content; /* బటన్ సైజు తగ్గకుండా చూస్తుంది */
        }

        .book-now-btn.desktop-only {
            display: inline-flex !important; /* 100% వ్యూలో బటన్ కనిపించేలా చేస్తుంది */
            background-color: #dfb160;
            color: #000;
            padding: 10px 22px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 700;
            transition: 0.3s;
            border: none;
            cursor: pointer;
        }

        /* Hero Overlay ఫిక్స్ (image_7560d4.jpg లోని లైన్ 341 ప్రకారం) */
        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.6);
            z-index: 1;
        }

        /* --- మీ ఒరిజినల్ స్టైల్స్ ఇక్కడి నుండి మొదలవుతాయి --- */
        .logo-section { display: flex; align-items: center; gap: 15px; }
        .custom-logo { height: 50px; border-radius: 50%; }
        .logo-text h1 { color: #dfb160; font-family: 'Playfair Display', serif; font-size: 22px; margin: 0; }
        .logo-text p { color: #fff; font-size: 10px; letter-spacing: 3px; margin: 0; }
        
        .nav-links { display: flex; gap: 30px; }
        .nav-links a { color: #fff; text-decoration: none; font-size: 15px; font-weight: 500; transition: 0.3s; }
        .nav-links a:hover, .nav-links a.active { color: #dfb160; }
        .mobile-only { display: none; }

        .hero-section {
            height: 85vh;
            background: url('hero_BG.jpeg') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            color: #fff;
        }

        .hero-content { z-index: 2; padding: 0 20px; }
        .welcome-text { color: #dfb160; letter-spacing: 4px; font-size: 14px; margin-bottom: 10px; }
        .hero-title { font-family: 'Playfair Display', serif; font-size: clamp(32px, 6vw, 60px); line-height: 1.1; margin-bottom: 15px; }
        .hero-location { font-size: 18px; color: #ccc; margin-bottom: 30px; }
        
        .hero-buttons { display: flex; gap: 20px; justify-content: center; flex-wrap: wrap; }
        .btn-whatsapp { background-color: #dfb160; color: #000; padding: 15px 30px; text-decoration: none; font-weight: bold; border-radius: 5px; }
        .btn-outline { border: 1px solid #fff; color: #fff; padding: 15px 30px; text-decoration: none; border-radius: 5px; }

        .hotels-section, .amenities-section, .discover-section { padding: 80px 5%; background-color: #111; color: #fff; }
        .section-title { text-align: center; font-family: 'Playfair Display', serif; font-size: 36px; color: #dfb160; margin-bottom: 50px; }
        
        .hotels-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .hotel-card { background: #1e1e1e; border: 1px solid #333; overflow: hidden; border-radius: 10px; }
        .hotel-card img { width: 100%; height: 250px; object-fit: cover; }
        .hotel-info { padding: 25px; }
        .btn-explore { display: inline-block; margin-top: 15px; color: #dfb160; text-decoration: none; font-weight: bold; }

        .amenities-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; }
        .amenity-card { background: #1a1a1a; padding: 30px; text-align: center; border-radius: 8px; border: 1px solid #333; transition: 0.3s; }
        .active-amenity { border-color: #dfb160; }
        .amenity-icon { font-size: 40px; color: #dfb160; margin-bottom: 20px; }

        .footer { background: #000; padding: 60px 5% 20px; border-top: 1px solid #333; color: #ccc; }
        .footer-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 40px; }
        .footer-title { color: #dfb160; margin-bottom: 20px; font-family: 'Playfair Display', serif; }
        .footer-links { list-style: none; }
        .footer-links li { margin-bottom: 10px; }
        .footer-links a { color: #ccc; text-decoration: none; }
        .footer-contact li { display: flex; gap: 10px; margin-bottom: 15px; }
        .footer-bottom { text-align: center; padding-top: 40px; border-top: 1px solid #222; margin-top: 40px; font-size: 13px; }

        /* మెనూ టాగుల్ */
        .menu-toggle { display: none; color: #fff; font-size: 24px; cursor: pointer; }

        @media (max-width: 992px) {
            .nav-links { display: none; position: absolute; top: 80px; left: 0; width: 100%; background: #111; flex-direction: column; padding: 20px; text-align: center; border-bottom: 1px solid #333; }
            .nav-links.active { display: flex; }
            .menu-toggle { display: block; }
            .desktop-only { display: none !important; }
            .mobile-only { display: block; margin-top: 10px; background: #dfb160; color: #000; padding: 12px; border-radius: 5px; }
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header class="navbar">
        <div class="logo-section">
            <div class="logo-icon">
                <img src="logo.png" alt="Logo" class="custom-logo">
            </div>
            <div class="logo-text">
                <h1>Madham Rajeshwari</h1>
                <p>COMPLEX</p>
            </div>
        </div>

        <nav class="nav-links" id="nav-links">
            <a href="index.html" class="active">Home</a>
            <a href="rooms.html">Rooms</a>
            <a href="temple-history.html">Temple History</a>
            <a href="contact.html">Contact</a>
            <button class="book-now-btn mobile-only" onclick="openBookingModal()">
                <i class="fa-solid fa-phone"></i> Book Now
            </button>
        </nav>

        <div class="right-section">
            <button class="book-now-btn desktop-only" onclick="openBookingModal()">
                <i class="fa-solid fa-phone"></i> Book Now
            </button>
            <div class="menu-toggle" id="mobile-menu">
                <i class="fa-solid fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero-section">
        <div class="hero-overlay"></div>
        <div class="hero-content">
            <p class="welcome-text">WELCOME TO</p>
            <h1 class="hero-title">Madham Rajeshwari<br>Complex</h1>
            <p class="hero-location">Ahobilam, Andhra Pradesh</p>
            <div class="hero-buttons">
                <a href="#" class="btn-whatsapp" onclick="openBookingModal(); return false;">Book via WhatsApp</a>
                <a href="#hotels" class="btn-outline">View Rooms</a>
            </div>
        </div>
    </section>

    <!-- Properties Section -->
    <section id="hotels" class="hotels-section">
        <h2 class="section-title">Our Properties</h2>
        <div class="hotels-container">
            <div class="hotel-card">
                <img src="MR-Complex.jpeg" alt="Madham Rajeshwari Complex">
                <div class="hotel-info">
                    <h3>Madham Rajeshwari Complex</h3>
                    <p>Experience comfortable stay with premium amenities near temples.</p>
                    <a href="madam-rajeswari-complex.html" class="btn-explore">Explore Complex</a>
                </div>
            </div>
            <div class="hotel-card">
                <img src="VB_House.jpeg" alt="Veerabadhra Complex">
                <div class="hotel-info">
                    <h3>Veerabadhra Complex</h3>
                    <p>Your perfect base for a spiritual journey in Ahobilam.</p>
                    <a href="veerabadhra-complex.html" class="btn-explore">Explore Hotel</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Amenities -->
    <section class="amenities-section">
        <h2 class="section-title">Our Amenities</h2>
        <div class="amenities-container">
            <div class="amenity-card">
                <i class="fa-solid fa-wind amenity-icon"></i>
                <h3>Air Conditioned</h3>
            </div>
            <div class="amenity-card active-amenity">
                <i class="fa-solid fa-wifi amenity-icon"></i>
                <h3>Free Wi-Fi</h3>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-shield-halved amenity-icon"></i>
                <h3>24/7 Security</h3>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-power-off amenity-icon"></i>
                <h3>Power Backup</h3>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-container">
            <div class="footer-col">
                <h3 class="footer-title">Contact Info</h3>
                <ul class="footer-contact">
                    <li><i class="fa-solid fa-location-dot"></i> Ahobilam, Andhra Pradesh</li>
                    <li><i class="fa-solid fa-phone"></i> +91 76759 62840</li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 Madham Rajeshwari Complex. All rights reserved.</p>
        </div>
    </footer>

    <!-- Booking Modal -->
    <div id="bookingModal" style="display:none; position:fixed; z-index:9999; left:0; top:0; width:100%; height:100%; background:rgba(0,0,0,0.9);">
        <div style="background:#1e1e1e; width:90%; max-width:400px; margin:10% auto; padding:30px; border:1px solid #dfb160; border-radius:10px; position:relative;">
            <span onclick="closeBookingModal()" style="position:absolute; right:20px; top:10px; color:#fff; cursor:pointer; font-size:24px;">&times;</span>
            <h3 style="color:#dfb160; text-align:center;">Book via WhatsApp</h3>
            <p style="color:#ccc; text-align:center; margin-top:10px;">Contact us directly to confirm your booking.</p>
            <a href="https://wa.me/917675962840" style="display:block; background:#25d366; color:#fff; text-align:center; padding:12px; margin-top:20px; text-decoration:none; border-radius:5px; font-weight:bold;">Chat on WhatsApp</a>
        </div>
    </div>

    <script>
        function openBookingModal() { document.getElementById('bookingModal').style.display = 'block'; }
        function closeBookingModal() { document.getElementById('bookingModal').style.display = 'none'; }
        
        const mobileMenu = document.getElementById('mobile-menu');
        const navLinks = document.getElementById('nav-links');
        mobileMenu.addEventListener('click', () => { navLinks.classList.toggle('active'); });
    </script>

</body>
</html>

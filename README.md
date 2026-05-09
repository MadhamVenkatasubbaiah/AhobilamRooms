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
        /* --- జూమ్ మరియు గ్యాప్ సమస్యల కోసం పక్కా ఫిక్స్ --- */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body, html {
            overflow-x: hidden;
            width: 100%;
            background-color: #111;
            font-family: 'Inter', sans-serif;
        }

        header.navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
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
            min-width: max-content;
        }

        .book-now-btn.desktop-only {
            display: inline-flex !important;
            background-color: #dfb160;
            color: #000;
            padding: 10px 22px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 700;
            cursor: pointer;
            border: none;
        }

        .logo-section { display: flex; align-items: center; gap: 15px; }
        .custom-logo { height: 50px; border-radius: 50%; }
        .logo-text h1 { color: #dfb160; font-family: 'Playfair Display', serif; font-size: 22px; margin: 0; }
        .logo-text p { color: #fff; font-size: 10px; letter-spacing: 3px; margin: 0; }
        
        .nav-links { display: flex; gap: 30px; }
        .nav-links a { color: #fff; text-decoration: none; font-size: 15px; transition: 0.3s; }
        .nav-links a:hover, .nav-links a.active { color: #dfb160; }

        /* Hero Section */
        .hero-section {
            height: 85vh;
            background: url('hero_BG.jpeg') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            color: #fff;
            text-align: center;
        }
        .hero-overlay {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.6); z-index: 1;
        }
        .hero-content { z-index: 2; }
        .hero-title { font-family: 'Playfair Display', serif; font-size: clamp(35px, 7vw, 65px); margin-bottom: 20px; }
        
        .hero-buttons { display: flex; gap: 20px; justify-content: center; margin-top: 30px; }
        .btn-whatsapp { background: #dfb160; color: #000; padding: 15px 30px; text-decoration: none; font-weight: bold; border-radius: 5px; }
        .btn-outline { border: 1px solid #fff; color: #fff; padding: 15px 30px; text-decoration: none; border-radius: 5px; }

        /* Sections Styling */
        .hotels-section, .amenities-section { padding: 80px 5%; background: #111; color: #fff; }
        .section-title { text-align: center; font-family: 'Playfair Display', serif; font-size: 36px; color: #dfb160; margin-bottom: 50px; }
        
        .hotels-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .hotel-card { background: #1e1e1e; border-radius: 10px; overflow: hidden; border: 1px solid #333; }
        .hotel-card img { width: 100%; height: 250px; object-fit: cover; }
        .hotel-info { padding: 25px; }

        /* Footer */
        .footer { background: #000; padding: 60px 5% 20px; color: #ccc; border-top: 1px solid #333; }
        .footer-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 40px; }
        .footer-col h3 { color: #dfb160; margin-bottom: 25px; font-family: 'Playfair Display', serif; }
        .footer-links { list-style: none; }
        .footer-links li { margin-bottom: 12px; }
        .footer-links a { color: #ccc; text-decoration: none; transition: 0.3s; }
        .footer-links a:hover { color: #dfb160; }
        .footer-contact li { display: flex; gap: 15px; margin-bottom: 20px; line-height: 1.5; list-style: none; }
        .footer-contact i { color: #dfb160; margin-top: 5px; }

        /* Mobile Menu */
        .menu-toggle { display: none; color: #fff; font-size: 24px; cursor: pointer; }
        @media (max-width: 992px) {
            .nav-links { display: none; position: absolute; top: 80px; left: 0; width: 100%; background: #111; flex-direction: column; padding: 20px; text-align: center; }
            .nav-links.active { display: flex; }
            .menu-toggle { display: block; }
            .desktop-only { display: none !important; }
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
            <p style="color:#dfb160; letter-spacing:4px; margin-bottom:10px;">WELCOME TO</p>
            <h1 class="hero-title">Madham Rajeshwari<br>Complex</h1>
            <p style="font-size:18px; color:#ccc;">Ahobilam, Andhra Pradesh</p>
            <div class="hero-buttons">
                <a href="#" class="btn-whatsapp" onclick="openBookingModal(); return false;">Book via WhatsApp</a>
                <a href="#hotels" class="btn-outline">View Rooms</a>
            </div>
        </div>
    </section>

    <!-- Properties -->
    <section id="hotels" class="hotels-section">
        <h2 class="section-title">Our Properties</h2>
        <div class="hotels-container">
            <div class="hotel-card">
                <img src="MR-Complex.jpeg" alt="MR Complex">
                <div class="hotel-info">
                    <h3>Madham Rajeshwari Complex</h3>
                    <p>Experience comfortable stay with premium amenities near temples.</p>
                    <a href="madam-rajeswari-complex.html" style="color:#dfb160; text-decoration:none; font-weight:bold; display:block; margin-top:15px;">Explore Complex →</a>
                </div>
            </div>
            <div class="hotel-card">
                <img src="VB_House.jpeg" alt="VB Complex">
                <div class="hotel-info">
                    <h3>Veerabadhra Complex</h3>
                    <p>Your perfect base for a spiritual journey in Ahobilam.</p>
                    <a href="veerabadhra-complex.html" style="color:#dfb160; text-decoration:none; font-weight:bold; display:block; margin-top:15px;">Explore Hotel →</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-container">
            <div class="footer-col">
                <h3>About Us</h3>
                <p>Madham Rajeshwari Complex provides the best hospitality services for pilgrims visiting the holy Nava Narasimha Kshetra, Ahobilam.</p>
            </div>
            <div class="footer-col">
                <h3>Quick Links</h3>
                <ul class="footer-links">
                    <li><a href="index.html">Home</a></li>
                    <li><a href="rooms.html">Rooms</a></li>
                    <li><a href="contact.html">Contact</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>Contact Info</h3>
                <ul class="footer-contact">
                    <li>
                        <i class="fa-solid fa-location-dot"></i>
                        <span>Madham Rajeshwari Complex, Lower Ahobilam, Kurnool Dist, AP - 518543</span>
                    </li>
                    <li>
                        <i class="fa-solid fa-phone"></i>
                        <span>+91 76759 62840</span>
                    </li>
                    <li>
                        <i class="fa-solid fa-envelope"></i>
                        <span>madhamvenkatasubbaiah363@gmail.com</span>
                    </li>
                </ul>
            </div>
        </div>
        <div style="text-align:center; margin-top:50px; padding-top:20px; border-top:1px solid #222; font-size:14px;">
            <p>&copy; 2026 Madham Rajeshwari Complex. All rights reserved.</p>
        </div>
    </footer>

    <!-- WhatsApp Modal -->
    <div id="bookingModal" style="display:none; position:fixed; z-index:9999; left:0; top:0; width:100%; height:100%; background:rgba(0,0,0,0.85); backdrop-filter:blur(5px);">
        <div style="background:#1e1e1e; width:90%; max-width:400px; margin:15% auto; padding:30px; border:1px solid #dfb160; border-radius:10px; position:relative; text-align:center;">
            <span onclick="closeBookingModal()" style="position:absolute; right:20px; top:10px; color:#fff; cursor:pointer; font-size:28px;">&times;</span>
            <h3 style="color:#dfb160; font-family:'Playfair Display'; font-size:24px;">Book Now</h3>
            <p style="color:#ccc; margin:20px 0;">Contact us on WhatsApp for room availability and pricing.</p>
            <a href="https://wa.me/917675962840" target="_blank" style="display:inline-block; background:#25d366; color:#fff; padding:12px 30px; text-decoration:none; border-radius:5px; font-weight:bold;">
                <i class="fa-brands fa-whatsapp"></i> Chat on WhatsApp
            </a>
        </div>
    </div>

    <script>
        function openBookingModal() { document.getElementById('bookingModal').style.display = 'block'; }
        function closeBookingModal() { document.getElementById('bookingModal').style.display = 'none'; }
        
        const mobileMenu = document.getElementById('mobile-menu');
        const navLinks = document.getElementById('nav-links');
        mobileMenu.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            const icon = mobileMenu.querySelector('i');
            icon.classList.toggle('fa-bars');
            icon.classList.toggle('fa-xmark');
        });

        window.onclick = function(event) {
            if (event.target == document.getElementById('bookingModal')) {
                closeBookingModal();
            }
        }
    </script>
</body>
</html>

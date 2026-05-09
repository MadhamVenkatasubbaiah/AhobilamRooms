<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Madham Rajeshwari Complex - Ahobilam</title>
    <!-- Fonts & Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

    <style>
        /* --- Base Reset --- */
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
            scroll-behavior: smooth;
        }

        /* --- Navbar Styles --- */
        header.navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            background-color: #111;
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid #333;
        }

        .logo-section { display: flex; align-items: center; gap: 15px; }
        .custom-logo { height: 50px; border-radius: 50%; }
        .logo-text h1 { color: #dfb160; font-family: 'Playfair Display', serif; font-size: 22px; margin: 0; }
        .logo-text p { color: #fff; font-size: 10px; letter-spacing: 3px; margin: 0; }

        .nav-links { display: flex; gap: 30px; align-items: center; }
        .nav-links a { color: #fff; text-decoration: none; font-size: 15px; transition: 0.3s; font-weight: 500; }
        .nav-links a:hover, .nav-links a.active { color: #dfb160; }

        .right-section { display: flex; align-items: center; gap: 15px; }

        .book-now-btn {
            background-color: #dfb160;
            color: #000;
            padding: 10px 22px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 700;
            cursor: pointer;
            border: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: 0.3s;
        }
        .book-now-btn:hover { background-color: #c99a4d; transform: translateY(-2px); }

        .menu-toggle { display: none; color: #fff; font-size: 24px; cursor: pointer; }

        /* --- Hero Section --- */
        .hero-section {
            height: 85vh;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('hero_BG.jpeg') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            text-align: center;
        }
        .hero-title { font-family: 'Playfair Display', serif; font-size: clamp(35px, 7vw, 65px); margin-bottom: 15px; line-height: 1.2; }
        .hero-buttons { display: flex; gap: 20px; justify-content: center; margin-top: 30px; }
        .btn-whatsapp { background: #dfb160; color: #000; padding: 15px 30px; text-decoration: none; font-weight: bold; border-radius: 5px; transition: 0.3s; }
        .btn-outline { border: 1px solid #fff; color: #fff; padding: 15px 30px; text-decoration: none; border-radius: 5px; transition: 0.3s; }
        .btn-outline:hover { background: #fff; color: #000; }

        /* --- Properties Section --- */
        .hotels-section { padding: 80px 5%; background: #111; color: #fff; }
        .section-title { text-align: center; font-family: 'Playfair Display', serif; font-size: 36px; color: #dfb160; margin-bottom: 50px; }
        .hotels-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .hotel-card { background: #1e1e1e; border-radius: 10px; overflow: hidden; border: 1px solid #333; transition: 0.3s; }
        .hotel-card:hover { border-color: #dfb160; }
        .hotel-card img { width: 100%; height: 250px; object-fit: cover; }
        .hotel-info { padding: 25px; }
        .hotel-info h3 { color: #dfb160; margin-bottom: 10px; }

        /* --- Booking Modal (Full Form) --- */
        .booking-modal {
            display: none; position: fixed; z-index: 10000; left: 0; top: 0; width: 100%; height: 100%;
            background-color: rgba(0,0,0,0.85); backdrop-filter: blur(5px);
        }
        .booking-modal-content {
            background-color: #1e1e1e; margin: 5vh auto; padding: 30px;
            border: 1px solid #dfb160; width: 90%; max-width: 500px;
            border-radius: 12px; position: relative; box-shadow: 0 10px 30px rgba(0,0,0,0.8);
            max-height: 90vh; overflow-y: auto;
        }
        .close-booking { position: absolute; right: 20px; top: 15px; color: #b3b3b3; font-size: 28px; cursor: pointer; }
        .form-group { margin-bottom: 15px; text-align: left; }
        .form-group label { display: block; color: #dfb160; margin-bottom: 5px; font-size: 14px; }
        .form-group input, .form-group select {
            width: 100%; padding: 12px; background: #2a2a2a; border: 1px solid #444; color: #fff; border-radius: 6px;
        }
        .date-group { display: flex; gap: 15px; }
        .submit-wa-btn {
            width: 100%; background-color: #25d366; color: #fff; border: none; padding: 14px;
            font-size: 16px; font-weight: bold; border-radius: 6px; cursor: pointer;
            display: flex; align-items: center; justify-content: center; gap: 10px; margin-top: 10px;
        }

        /* --- Footer --- */
        .footer { background: #000; padding: 60px 5% 20px; color: #ccc; border-top: 1px solid #333; }
        .footer-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 40px; }
        .footer-col h3 { color: #dfb160; margin-bottom: 25px; font-family: 'Playfair Display', serif; }
        .footer-contact li { display: flex; gap: 15px; margin-bottom: 20px; list-style: none; }
        .footer-contact i { color: #dfb160; }

        /* --- Responsive --- */
        @media (max-width: 992px) {
            .nav-links { display: none; position: absolute; top: 80px; left: 0; width: 100%; background: #111; flex-direction: column; padding: 30px; }
            .nav-links.active { display: flex; border-bottom: 1px solid #333; }
            .menu-toggle { display: block; }
            .desktop-hide { display: none; }
        }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header class="navbar">
        <div class="logo-section">
            <img src="logo.png" alt="Logo" class="custom-logo">
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
            <!-- Mobile Only Book Button -->
            <button class="book-now-btn desktop-hide" onclick="openBookingModal()">
                <i class="fa-solid fa-phone"></i> Book Now
            </button>
        </nav>

        <div class="right-section">
            <button class="book-now-btn" id="header-book-btn" onclick="openBookingModal()">
                <i class="fa-solid fa-phone"></i> Book Now
            </button>
            <div class="menu-toggle" id="mobile-menu">
                <i class="fa-solid fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero-section">
        <div class="hero-content">
            <p style="color:#dfb160; letter-spacing:4px; margin-bottom:10px; font-weight:bold;">WELCOME TO</p>
            <h1 class="hero-title">Madham Rajeshwari<br>Complex</h1>
            <p style="font-size:18px; color:#ccc; margin-bottom:20px;">Ahobilam, Andhra Pradesh</p>
            <div class="hero-buttons">
                <a href="#" class="btn-whatsapp" onclick="openBookingModal(); return false;">Book via WhatsApp</a>
                <a href="#hotels" class="btn-outline">View Properties</a>
            </div>
        </div>
    </section>

    <!-- Properties Section -->
    <section id="hotels" class="hotels-section">
        <h2 class="section-title">Our Properties</h2>
        <div class="hotels-container">
            <div class="hotel-card">
                <img src="MR-Complex.jpeg" alt="MR Complex">
                <div class="hotel-info">
                    <h3>Madham Rajeshwari Complex</h3>
                    <p>Experience comfortable stay with premium amenities near the sacred Ahobilam temples.</p>
                    <a href="madam-rajeswari-complex.html" style="color:#dfb160; text-decoration:none; font-weight:bold; display:block; margin-top:15px;">Explore Complex →</a>
                </div>
            </div>
            <div class="hotel-card">
                <img src="VB_House.jpeg" alt="VB Complex">
                <div class="hotel-info">
                    <h3>Veerabadhra Complex</h3>
                    <p>Your perfect base for a spiritual journey with excellent hospitality and care.</p>
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
                <p>Providing divine hospitality near the sacred Nava Narasimha temples. Comfortable stay with modern amenities.</p>
            </div>
            <div class="footer-col">
                <h3>Quick Links</h3>
                <ul style="list-style:none;">
                    <li><a href="index.html" style="color:#ccc; text-decoration:none;">Home</a></li>
                    <li><a href="rooms.html" style="color:#ccc; text-decoration:none;">Rooms</a></li>
                    <li><a href="contact.html" style="color:#ccc; text-decoration:none;">Contact</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>Contact Info</h3>
                <ul class="footer-contact">
                    <li><i class="fa-solid fa-location-dot"></i> Ahobilam, Andhra Pradesh, India</li>
                    <li><i class="fa-solid fa-phone"></i> +91 76759 62840</li>
                    <li><i class="fa-solid fa-envelope"></i> madhamvenkatasubbaiah363@gmail.com</li>
                </ul>
            </div>
        </div>
        <div style="text-align:center; margin-top:40px; color:#666; font-size:14px;">
            &copy; 2026 Madham Rajeshwari Complex. All rights reserved.
        </div>
    </footer>

    <!-- Booking Modal Form -->
    <div id="bookingModal" class="booking-modal">
        <div class="booking-modal-content">
            <span class="close-booking" onclick="closeBookingModal()">&times;</span>
            <h3 style="color:#dfb160; font-family:'Playfair Display'; font-size:24px; margin-bottom:20px; text-align:center; border-bottom:1px dashed #444; padding-bottom:10px;">Book Your Stay</h3>
            
            <form id="whatsappBookingForm" onsubmit="sendWhatsApp(event)">
                <div class="form-group">
                    <label>Full Name *</label>
                    <input type="text" id="b_name" placeholder="Enter your name" required>
                </div>
                <div class="form-group">
                    <label>Select Property *</label>
                    <select id="b_hotel" required>
                        <option value="Madham Rajeshwari Complex">Madham Rajeshwari Complex</option>
                        <option value="Veerabadhra Complex">Veerabadhra Complex</option>
                    </select>
                </div>
                <div class="date-group">
                    <div class="form-group" style="flex:1;">
                        <label>Check-in *</label>
                        <input type="date" id="b_checkin" required>
                    </div>
                    <div class="form-group" style="flex:1;">
                        <label>Check-out *</label>
                        <input type="date" id="b_checkout" required>
                    </div>
                </div>
                <div class="date-group">
                    <div class="form-group" style="flex:1;">
                        <label>Persons *</label>
                        <input type="number" id="b_persons" min="1" value="1" required>
                    </div>
                    <div class="form-group" style="flex:1;">
                        <label>Room Type *</label>
                        <select id="b_roomtype" required>
                            <option value="AC Room">AC Room</option>
                            <option value="Non-AC Room">Non-AC Room</option>
                        </select>
                    </div>
                </div>
                <button type="submit" class="submit-wa-btn">
                    <i class="fa-brands fa-whatsapp"></i> Send Booking Request
                </button>
            </form>
        </div>
    </div>

    <script>
        // Set min date to today
        const today = new Date().toISOString().split('T')[0];
        document.getElementById("b_checkin").setAttribute('min', today);
        document.getElementById("b_checkout").setAttribute('min', today);

        function openBookingModal() { document.getElementById('bookingModal').style.display = 'block'; }
        function closeBookingModal() { document.getElementById('bookingModal').style.display = 'none'; }

        // Mobile Menu Logic
        const mobileMenu = document.getElementById('mobile-menu');
        const navLinks = document.getElementById('nav-links');
        mobileMenu.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            const icon = mobileMenu.querySelector('i');
            icon.classList.toggle('fa-bars');
            icon.classList.toggle('fa-xmark');
        });

        // WhatsApp Logic
        function sendWhatsApp(e) {
            e.preventDefault();
            const name = document.getElementById('b_name').value;
            const hotel = document.getElementById('b_hotel').value;
            const checkin = document.getElementById('b_checkin').value;
            const checkout = document.getElementById('b_checkout').value;
            const persons = document.getElementById('b_persons').value;
            const roomType = document.getElementById('b_roomtype').value;

            const message = `*NEW BOOKING REQUEST*%0A%0A*Name:* ${name}%0A*Property:* ${hotel}%0A*Check-in:* ${checkin}%0A*Check-out:* ${checkout}%0A*Persons:* ${persons}%0A*Room:* ${roomType}`;
            
            window.open(`https://wa.me/917675962840?text=${message}`, '_blank');
            closeBookingModal();
        }

        // Close on outside click
        window.onclick = function(event) {
            if (event.target == document.getElementById('bookingModal')) { closeBookingModal(); }
        }
    </script>
</body>
</html>

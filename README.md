<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Madham Rajeshwari Complex - Ahobilam</title>
    <!-- CSS Link -->
    <link rel="stylesheet" href="style.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

    <style>
        /* --- మీ పాత కోడ్ లో ఉన్న CSS ని ఇక్కడ మోడిఫై చేశాను --- */
        
        :root {
            --primary-gold: #dfb160; /* స్క్రీన్‌షాట్ లో ఉన్న గోల్డ్ కలర్ */
            --dark-bg: #111111;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            background-color: rgba(0,0,0,0.95);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid #333;
        }

        /* జూమ్ ఇష్యూ ని ఫిక్స్ చేసే ముఖ్యమైన మార్పు ఇక్కడ ఉంది */
        .right-section {
            display: flex !important;
            align-items: center !important;
            gap: 15px;
            min-width: max-content; /* ఇది బటన్ ని ఎప్పుడూ కనిపించేలా చేస్తుంది */
        }

        .book-now-btn {
            background-color: var(--primary-gold);
            color: #000;
            padding: 10px 22px;
            border-radius: 4px;
            font-weight: 700;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: 0.3s;
            white-space: nowrap; /* టెక్స్ట్ విరగకుండా చేస్తుంది */
        }

        .desktop-only {
            display: inline-flex !important; /* 100% వ్యూ లో కూడా కనిపించడానికి */
        }

        @media screen and (max-width: 768px) {
            .desktop-only { display: none !important; }
            .mobile-only { display: inline-flex !important; }
        }

        /* ఫుటర్ స్టైల్స్ (మీ స్క్రీన్‌షాట్ ప్రకారం) */
        .footer {
            background-color: var(--dark-bg);
            color: #999;
            padding: 50px 5% 20px;
            font-family: 'Inter', sans-serif;
        }

        .footer-title {
            color: var(--primary-gold);
            font-family: 'Playfair Display', serif;
            margin-bottom: 20px;
            font-size: 22px;
        }

        .footer-links li a, .footer-contact li {
            color: #ccc;
            text-decoration: none;
            margin-bottom: 10px;
            display: block;
            font-size: 14px;
        }

        .footer-contact i {
            color: var(--primary-gold);
            margin-right: 10px;
        }

        /* ఇతర సెక్షన్లు */
        .section-title {
            color: var(--primary-gold);
            text-align: center;
            font-family: 'Playfair Display', serif;
            font-size: 32px;
            margin-bottom: 40px;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header class="navbar">
        <div class="logo-section">
            <div class="logo-text">
                <h1 style="color: var(--primary-gold); margin: 0; font-family: 'Playfair Display';">Madham Rajeshwari</h1>
                <p style="margin: 0; color: #888; letter-spacing: 2px; font-size: 10px;">COMPLEX</p>
            </div>
        </div>

        <nav class="nav-links" id="nav-links">
            <a href="index.html" class="active" style="color:#fff; margin: 0 15px; text-decoration: none;">Home</a>
            <a href="rooms.html" style="color:#fff; margin: 0 15px; text-decoration: none;">Rooms</a>
            <a href="temple-history.html" style="color:#fff; margin: 0 15px; text-decoration: none;">Temple History</a>
            <a href="contact.html" style="color:#fff; margin: 0 15px; text-decoration: none;">Contact</a>
        </nav>

        <div class="right-section">
            <button class="book-now-btn desktop-only" onclick="openBookingModal()">
                <i class="fa-solid fa-phone"></i> Book Now
            </button>
            <div class="menu-toggle" id="mobile-menu" style="color: #fff; cursor: pointer; font-size: 20px;">
                <i class="fa-solid fa-bars"></i>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero-section" style="background-image: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('hero_BG.jpeg'); background-size: cover; height: 80vh; display: flex; align-items: center; justify-content: center; text-align: center; color: #fff;">
        <div class="hero-content">
            <p style="letter-spacing: 4px; font-size: 14px;">WELCOME TO</p>
            <h1 style="font-size: 50px; font-family: 'Playfair Display'; margin: 10px 0;">Madham Rajeshwari Complex</h1>
            <p style="font-size: 18px; color: #ddd;">Ahobilam, Andhra Pradesh</p>
            <div style="margin-top: 30px;">
                <a href="#" class="book-now-btn" onclick="openBookingModal(); return false;" style="background-color: #25d366; color: #fff; margin-right: 15px;">Book via WhatsApp</a>
                <a href="#hotels" class="book-now-btn" style="background: transparent; border: 1px solid #fff; color: #fff;">Our Rooms</a>
            </div>
        </div>
    </section>

    <!-- Amenities (409 లైన్ల కోడ్ లో ఉన్న టెక్స్ట్ ఇక్కడ ఉంది) -->
    <section id="amenities" style="padding: 60px 5%;">
        <h2 class="section-title">Our Amenities</h2>
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px;">
            <div style="text-align: center; padding: 20px; border: 1px solid #eee;">
                <i class="fa-solid fa-wind" style="font-size: 30px; color: var(--primary-gold);"></i>
                <h3 style="margin-top: 15px;">Air Conditioned</h3>
                <p style="font-size: 14px; color: #666;">Full comfort in every room</p>
            </div>
            <div style="text-align: center; padding: 20px; border: 1px solid #eee;">
                <i class="fa-solid fa-wifi" style="font-size: 30px; color: var(--primary-gold);"></i>
                <h3 style="margin-top: 15px;">Free Wi-Fi</h3>
                <p style="font-size: 14px; color: #666;">Stay connected always</p>
            </div>
            <!-- ఇతర Amenities అన్నీ ఇక్కడ రిపీట్ అవుతాయి -->
        </div>
    </section>

    <!-- Footer (As per image_75f280.png) -->
    <footer class="footer">
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 40px; max-width: 1200px; margin: 0 auto;">
            <div class="footer-col">
                <h3 class="footer-title">Madham Rajeshwari Complex</h3>
                <p>Your comfortable stay near the sacred Ahobilam temples. Experience divine hospitality with modern amenities.</p>
            </div>
            <div class="footer-col">
                <h3 class="footer-title">Quick Links</h3>
                <ul class="footer-links" style="list-style: none; padding: 0;">
                    <li><a href="index.html">Home</a></li>
                    <li><a href="rooms.html">Rooms</a></li>
                    <li><a href="temple-history.html">Temple History</a></li>
                    <li><a href="contact.html">Contact</a></li>
                    <li><a href="#">Terms & Conditions</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3 class="footer-title">Contact Info</h3>
                <ul class="footer-contact" style="list-style: none; padding: 0;">
                    <li><i class="fa-solid fa-location-dot"></i> Ahobilam, Kurnool District, Andhra Pradesh, India</li>
                    <li><i class="fa-solid fa-phone"></i> +91 76759 62840</li>
                    <li><i class="fa-solid fa-envelope"></i> madhamvenkatasubbaiah363@gmail.com</li>
                </ul>
            </div>
        </div>
        <div style="text-align: center; margin-top: 50px; padding-top: 20px; border-top: 1px solid #222; font-size: 13px;">
            <p>&copy; 2026 Madham Rajeshwari Complex. All rights reserved.</p>
        </div>
    </footer>

    <!-- Booking Modal -->
    <div id="bookingModal" style="display: none; position: fixed; z-index: 9999; left: 0; top: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.9); overflow-y: auto;">
        <div style="background: #222; margin: 5% auto; padding: 30px; width: 90%; max-width: 500px; border-radius: 10px; border: 1px solid var(--primary-gold); color: #fff;">
            <span onclick="closeBookingModal()" style="float: right; cursor: pointer; font-size: 28px;">&times;</span>
            <h2 style="color: var(--primary-gold); text-align: center;">Book Your Stay</h2>
            <form onsubmit="sendWhatsApp(event)" style="margin-top: 20px;">
                <input type="text" id="name" placeholder="Your Name" required style="width: 100%; padding: 12px; margin-bottom: 15px; background: #333; border: 1px solid #444; color: #fff;">
                <select id="hotel" required style="width: 100%; padding: 12px; margin-bottom: 15px; background: #333; border: 1px solid #444; color: #fff;">
                    <option value="Madham Rajeshwari Complex">Madham Rajeshwari Complex</option>
                    <option value="Veerabadhra Complex">Veerabadhra Complex</option>
                </select>
                <div style="display: flex; gap: 10px;">
                    <input type="date" id="checkin" required style="flex: 1; padding: 12px; margin-bottom: 15px; background: #333; border: 1px solid #444; color: #fff;">
                    <input type="date" id="checkout" required style="flex: 1; padding: 12px; margin-bottom: 15px; background: #333; border: 1px solid #444; color: #fff;">
                </div>
                <button type="submit" style="width: 100%; padding: 15px; background: #25d366; border: none; color: #fff; font-weight: bold; cursor: pointer; border-radius: 5px;">
                    <i class="fa-brands fa-whatsapp"></i> Send Booking via WhatsApp
                </button>
            </form>
        </div>
    </div>

    <script>
        // Modal logic
        function openBookingModal() { document.getElementById('bookingModal').style.display = 'block'; }
        function closeBookingModal() { document.getElementById('bookingModal').style.display = 'none'; }

        // Mobile Menu
        const mobileMenu = document.getElementById('mobile-menu');
        const navLinks = document.getElementById('nav-links');
        mobileMenu.addEventListener('click', () => { navLinks.classList.toggle('active'); });

        // WhatsApp redirect
        function sendWhatsApp(e) {
            e.preventDefault();
            const name = document.getElementById('name').value;
            const hotel = document.getElementById('hotel').value;
            const checkin = document.getElementById('checkin').value;
            const msg = `*NEW BOOKING*\nName: ${name}\nHotel: ${hotel}\nCheck-in: ${checkin}`;
            window.open(`https://wa.me/917675962840?text=${encodeURIComponent(msg)}`, '_blank');
        }

        window.onclick = function(event) {
            if (event.target == document.getElementById('bookingModal')) closeBookingModal();
        }
    </script>

</body>
</html>

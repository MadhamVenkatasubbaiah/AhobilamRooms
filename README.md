<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Madham Rajeshwari Complex - Ahobilam</title>
    <!-- CSS లింక్ -->
    <link rel="stylesheet" href="style.css">
    <!-- ఫాంట్స్ -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@400;500&display=swap" rel="stylesheet">
    <!-- ఐకాన్స్ -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

    <style>
        /* జూమ్ సమస్యను పరిష్కరించడానికి అవసరమైన CSS */
        :root {
            --primary-gold: #dfb160;
            --dark-bg: #1e1e1e;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            background: rgba(0,0,0,0.9);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .right-section {
            display: flex;
            align-items: center;
            gap: 15px;
            min-width: fit-content; /* బటన్ కంప్రెస్ అవ్వకుండా చేస్తుంది */
        }

        /* బటన్ స్టైల్స్ */
        .book-now-btn {
            background-color: var(--primary-gold);
            color: #000;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            font-weight: 700;
            cursor: pointer;
            text-decoration: none;
            transition: 0.3s;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            white-space: nowrap;
        }

        /* డెస్క్‌టాప్ మరియు మొబైల్ విజిబిలిటీ ఫిక్స్ */
        @media screen and (min-width: 769px) {
            .mobile-only { display: none !important; }
            .desktop-only { display: inline-flex !important; }
        }

        @media screen and (max-width: 768px) {
            .desktop-only { display: none !important; }
            .mobile-only { display: inline-flex !important; }
            .nav-links {
                display: none; /* మొబైల్ మెనూ లాజిక్ */
            }
            .nav-links.active {
                display: flex;
                flex-direction: column;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: var(--dark-bg);
                padding: 20px;
            }
        }

        /* Hero Section Fix */
        .hero-section {
            background-image: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('hero_BG.jpeg');
            background-size: cover;
            background-position: center;
            min-height: 80vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: #fff;
        }

        /* Modal Styles */
        .booking-modal {
            display: none;
            position: fixed;
            z-index: 2000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.9);
            backdrop-filter: blur(5px);
        }

        .booking-modal-content {
            background-color: #2a2a2a;
            margin: 5% auto;
            padding: 30px;
            width: 90%;
            max-width: 500px;
            border-radius: 15px;
            border: 1px solid var(--primary-gold);
            color: #fff;
        }

        .form-group { margin-bottom: 15px; }
        .form-group input, .form-group select {
            width: 100%;
            padding: 12px;
            margin-top: 5px;
            background: #1e1e1e;
            border: 1px solid #444;
            color: #fff;
            border-radius: 5px;
        }
    </style>
</head>
<body>

    <header class="navbar">
        <div class="logo-section">
            <div class="logo-text">
                <h1 style="color: var(--primary-gold); margin:0;">Madham Rajeshwari</h1>
                <p style="margin:0; letter-spacing: 2px; font-size: 12px; color: #ccc;">COMPLEX</p>
            </div>
        </div>

        <nav class="nav-links" id="nav-links">
            <a href="index.html" style="color:#fff; text-decoration:none; margin: 0 15px;">Home</a>
            <a href="rooms.html" style="color:#fff; text-decoration:none; margin: 0 15px;">Rooms</a>
            <a href="temple-history.html" style="color:#fff; text-decoration:none; margin: 0 15px;">Temple History</a>
            <a href="contact.html" style="color:#fff; text-decoration:none; margin: 0 15px;">Contact</a>
        </nav>

        <div class="right-section">
            <button class="book-now-btn desktop-only" onclick="openBookingModal()">
                <i class="fa-solid fa-phone"></i> Book Now
            </button>
            <div class="menu-toggle" id="mobile-menu" style="color:#fff; font-size: 24px; cursor:pointer;">
                <i class="fa-solid fa-bars"></i>
            </div>
        </div>
    </header>

    <section class="hero-section">
        <div class="hero-content">
            <p style="letter-spacing: 3px;">WELCOME TO</p>
            <h1 style="font-size: 3rem; margin: 10px 0;">Madham Rajeshwari Complex</h1>
            <p>Ahobilam, Andhra Pradesh</p>
            <div style="margin-top: 30px;">
                <a href="#" class="book-now-btn" onclick="openBookingModal(); return false;" style="background:#25d366; color:#fff;">Book via WhatsApp</a>
                <a href="#hotels" class="book-now-btn" style="background:transparent; border: 1px solid #fff; color:#fff; margin-left:10px;">View Properties</a>
            </div>
        </div>
    </section>

    <!-- Properties Section -->
    <section id="hotels" style="padding: 60px 5%; background: #f9f9f9;">
        <h2 style="text-align:center; margin-bottom: 40px;">Our Properties</h2>
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px;">
            <div class="hotel-card" style="background:#fff; border-radius: 10px; overflow:hidden; box-shadow: 0 5px 15px rgba(0,0,0,0.1);">
                <img src="MR-Complex.jpeg" style="width:100%; height:250px; object-fit:cover;">
                <div style="padding: 20px;">
                    <h3>Madham Rajeshwari Complex</h3>
                    <p>Experience comfortable stay with premium amenities near the sacred Ahobilam temples.</p>
                    <a href="madam-rajeswari-complex.html" style="color:var(--primary-gold); font-weight:bold;">Explore Complex →</a>
                </div>
            </div>
            <div class="hotel-card" style="background:#fff; border-radius: 10px; overflow:hidden; box-shadow: 0 5px 15px rgba(0,0,0,0.1);">
                <img src="VB_House.jpeg" style="width:100%; height:250px; object-fit:cover;">
                <div style="padding: 20px;">
                    <h3>Veerabadhra Complex</h3>
                    <p>Your perfect base for a spiritual journey with excellent hospitality and care.</p>
                    <a href="veerabadhra-complex.html" style="color:var(--primary-gold); font-weight:bold;">Explore Hotel →</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Booking Modal -->
    <div id="bookingModal" class="booking-modal">
        <div class="booking-modal-content">
            <span onclick="closeBookingModal()" style="float:right; cursor:pointer; font-size: 24px;">&times;</span>
            <h3 style="color:var(--primary-gold);">Book Your Stay</h3>
            <form onsubmit="sendWhatsApp(event)">
                <div class="form-group">
                    <label>Full Name</label>
                    <input type="text" id="b_name" required>
                </div>
                <div class="form-group">
                    <label>Select Property</label>
                    <select id="b_hotel" required>
                        <option value="Madham Rajeshwari Complex">Madham Rajeshwari Complex</option>
                        <option value="Veerabadhra Complex">Veerabadhra Complex</option>
                    </select>
                </div>
                <div style="display:flex; gap:10px;">
                    <div class="form-group" style="flex:1;">
                        <label>Check-in</label>
                        <input type="date" id="b_checkin" required>
                    </div>
                    <div class="form-group" style="flex:1;">
                        <label>Check-out</label>
                        <input type="date" id="b_checkout" required>
                    </div>
                </div>
                <button type="submit" class="book-now-btn" style="width:100%; justify-content:center; background:#25d366; color:#fff; margin-top:10px;">
                    <i class="fa-brands fa-whatsapp"></i> Send WhatsApp Request
                </button>
            </form>
        </div>
    </div>

    <footer style="background:#111; color:#999; padding: 40px 5%; text-align:center;">
        <p>Ahobilam, Andhra Pradesh | +91 76759 62840</p>
        <p>&copy; 2026 Madham Rajeshwari Complex. All rights reserved.</p>
    </footer>

    <script>
        // Mobile Menu Toggle
        const mobileMenu = document.getElementById('mobile-menu');
        const navLinks = document.getElementById('nav-links');
        mobileMenu.onclick = () => navLinks.classList.toggle('active');

        // Modal Functions
        function openBookingModal() { document.getElementById('bookingModal').style.display = 'block'; }
        function closeBookingModal() { document.getElementById('bookingModal').style.display = 'none'; }

        // WhatsApp Logic
        function sendWhatsApp(e) {
            e.preventDefault();
            const name = document.getElementById('b_name').value;
            const hotel = document.getElementById('b_hotel').value;
            const msg = `*NEW BOOKING*\nName: ${name}\nHotel: ${hotel}\nCheck-in: ${document.getElementById('b_checkin').value}`;
            window.open(`https://wa.me/917675962840?text=${encodeURIComponent(msg)}`, '_blank');
        }

        window.onclick = (event) => {
            if (event.target == document.getElementById('bookingModal')) closeBookingModal();
        }
    </script>
</body>
</html>

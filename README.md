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
        /* మీ బ్యాక్‌గ్రౌండ్ ఫోటో మరియు ఇతర స్టైల్స్ ఇక్కడ ఉన్నాయి */
        .hero-section {
            background-image: url('hero_BG.jpeg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            position: relative;
            min-height: 80vh; /* హైట్ కోసం */
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .hero-overlay {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            background-color: rgba(0, 0, 0, 0.6);
            z-index: 1;
        }

        .hero-content {
            position: relative; z-index: 2;
            text-align: center;
            color: #fff;
        }

        /* ఫామ్ పాప్-అప్ డిజైన్ */
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
        .close-booking {
            position: absolute; right: 20px; top: 15px; color: #b3b3b3;
            font-size: 28px; font-weight: bold; cursor: pointer; transition: 0.3s;
        }
        .close-booking:hover { color: #dfb160; }
        .booking-modal-content h3 {
            color: #dfb160; text-align: center; margin-bottom: 25px;
            font-family: 'Playfair Display', serif; font-size: 26px; border-bottom: 1px dashed #444; padding-bottom: 10px;
        }
        
        .form-group { margin-bottom: 18px; }
        .form-group label { display: block; color: #b3b3b3; margin-bottom: 6px; font-size: 14px; font-weight: 500;}
        .form-group input, .form-group select {
            width: 100%; padding: 12px; background-color: #2a2a2a;
            border: 1px solid #444; color: #fff; border-radius: 6px;
            font-family: 'Inter', sans-serif; font-size: 15px; transition: 0.3s;
        }
        .form-group input:focus, .form-group select:focus {
            outline: none; border-color: #dfb160; box-shadow: 0 0 5px rgba(223, 177, 96, 0.3);
        }
        .date-group { display: flex; gap: 15px; }
        .date-group .form-group { width: 50%; }
        
        .submit-wa-btn {
            width: 100%; background-color: #25d366; color: #fff; border: none;
            padding: 14px; font-size: 16px; font-weight: bold; border-radius: 6px;
            cursor: pointer; display: flex; align-items: center; justify-content: center; gap: 10px;
            margin-top: 10px; transition: 0.3s;
        }
        .submit-wa-btn:hover { background-color: #1ebd57; transform: translateY(-2px); }
        ::-webkit-calendar-picker-indicator { filter: invert(1); cursor: pointer; }
    </style>
</head>
<body>

    <!-- Header Section -->
    <header class="navbar">
        <div class="logo-section">
            <div class="logo-icon">
                <img src="logo.png" alt="Madham Rajeshwari Logo" class="custom-logo">
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
            <p class="hero-tagline">Your divine stay near the sacred Narasimha temples</p>
            
            <div class="hero-buttons">
                <a href="#" class="btn-whatsapp" onclick="openBookingModal(); return false;">Book via WhatsApp</a>
                <a href="#hotels" class="btn-outline">View Rooms</a>
            </div>
        </div>
    </section>

    <!-- Our Properties Section -->
    <section id="hotels" class="hotels-section">
        <h2 class="section-title">Our Properties</h2>
        <div class="hotels-container">
            <div class="hotel-card">
                <img src="MR-Complex.jpeg" alt="Madham Rajeshwari Complex">
                <div class="hotel-info">
                    <h3>Madham Rajeshwari Complex</h3>
                    <p>Experience comfortable stay with premium amenities near the sacred Ahobilam temples.</p>
                    <a href="madam-rajeswari-complex.html" class="btn-explore">Explore Complex</a>
                </div>
            </div>

            <div class="hotel-card">
                <img src="VB_House.jpeg" alt="Veerabadhra Complex">
                <div class="hotel-info">
                    <h3>Veerabadhra Complex</h3> 
                    <p>Your perfect base for a spiritual journey with excellent hospitality and care.</p>
                    <a href="veerabadhra-complex.html" class="btn-explore">Explore Hotel</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Our Amenities Section -->
    <section id="amenities" class="amenities-section">
        <h2 class="section-title">Our Amenities</h2>
        <div class="amenities-container">
            <div class="amenity-card">
                <i class="fa-solid fa-wind amenity-icon"></i>
                <h3>Air Conditioned</h3>
                <p>All rooms are fully air conditioned</p>
            </div>
            <div class="amenity-card">
                <i class="fa-regular fa-star amenity-icon"></i>
                <h3>King Size Beds</h3>
                <p>Premium king size beds for comfort</p>
            </div>
            <div class="amenity-card active-amenity">
                <i class="fa-solid fa-wifi amenity-icon"></i>
                <h3>Free Wi-Fi</h3>
                <p>Complimentary high-speed internet</p>
            </div>
            <div class="amenity-card">
                <i class="fa-solid fa-shield-halved amenity-icon"></i>
                <h3>24/7 Security</h3>
                <p>Round the clock security & reception</p>
            </div>
        </div>
    </section>

    <!-- Discover Ahobilam Section -->
    <section id="history" class="discover-section">
        <div class="discover-container">
            <div class="discover-content">
                <span class="sub-heading">DISCOVER</span>
                <h2 class="discover-title">Ahobilam – The Sacred Abode</h2>
                <p>Ahobilam is a highly revered pilgrimage center nestled in the lush Nallamala Hills of Andhra Pradesh. Known as the 'Nava Narasimha Kshetram,' it is the only place where Lord Narasimha is worshipped in nine distinct forms.</p>
                <p>Our hotel is conveniently located near the temple complex, offering a serene, comfortable, and highly accessible base for your spiritual journey.</p>
                <a href="temple-history.html" class="learn-more-link">
                    <i class="fa-solid fa-location-dot"></i> Learn more about Ahobilam
                </a>
            </div>
            <div class="discover-image">
                <img src="abm.jpg" alt="Ahobilam Temple Landscape">
            </div>
        </div>
    </section>

    <!-- Footer Section -->
    <footer id="contact" class="footer">
        <div class="footer-container">
            <div class="footer-col">
                <h3 class="footer-title">Madham Rajeshwari Complex</h3>
                <p>Your comfortable stay near the sacred Ahobilam temples. Experience divine hospitality with modern amenities.</p>
            </div>
            <div class="footer-col">
                <h3 class="footer-title">Quick Links</h3>
                <ul class="footer-links">
                    <li><a href="index.html">Home</a></li>
                    <li><a href="rooms.html">Rooms</a></li>
                    <li><a href="temple-history.html">Temple History</a></li>
                    <li><a href="contact.html">Contact</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3 class="footer-title">Contact Info</h3>
                <ul class="footer-contact">
                    <li><i class="fa-solid fa-location-dot"></i> Ahobilam, Kurnool District, Andhra Pradesh, India</li>
                    <li><i class="fa-solid fa-phone"></i> +91 76759 62840</li>
                    <li><i class="fa-solid fa-envelope"></i> madhamvenkatasubbaiah363@gmail.com</li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 Madham Rajeshwari Complex. All rights reserved.</p>
        </div>
    </footer>

    <!-- Booking Form Modal -->
    <div id="bookingModal" class="booking-modal">
        <div class="booking-modal-content">
            <span class="close-booking" onclick="closeBookingModal()">&times;</span>
            <h3>Book Your Stay</h3>
            <form id="whatsappBookingForm" onsubmit="sendWhatsApp(event)">
                <div class="form-group">
                    <label>Full Name *</label>
                    <input type="text" id="b_name" placeholder="Enter your name" required>
                </div>
                <div class="form-group">
                    <label>Select Hotel *</label>
                    <select id="b_hotel" required>
                        <option value="">-- Choose Property --</option>
                        <option value="Madham Rajeshwari Complex">Madham Rajeshwari Complex</option>
                        <option value="Veerabadhra Complex">Veerabadhra Complex</option>
                    </select>
                </div>
                <div class="date-group">
                    <div class="form-group">
                        <label>Check-in Date *</label>
                        <input type="date" id="b_checkin" required>
                    </div>
                    <div class="form-group">
                        <label>Check-out Date *</label>
                        <input type="date" id="b_checkout" required>
                    </div>
                </div>
                <div class="date-group">
                    <div class="form-group">
                        <label>No. of Persons *</label>
                        <input type="number" id="b_persons" min="1" placeholder="Ex: 2" required>
                    </div>
                    <div class="form-group">
                        <label>Room Preference *</label>
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
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenu = document.getElementById('mobile-menu');
            const navLinks = document.getElementById('nav-links');
            
            if(mobileMenu && navLinks) {
                const icon = mobileMenu.querySelector('i');
                mobileMenu.addEventListener('click', function() {
                    navLinks.classList.toggle('active');
                    if(navLinks.classList.contains('active')) {
                        icon.classList.replace('fa-bars', 'fa-xmark');
                    } else {
                        icon.classList.replace('fa-xmark', 'fa-bars');
                    }
                });
            }

            // Date constraints
            const today = new Date().toISOString().split('T')[0];
            document.getElementById("b_checkin").setAttribute('min', today);
            document.getElementById("b_checkout").setAttribute('min', today);
        });

        function openBookingModal() {
            document.getElementById('bookingModal').style.display = 'block';
        }

        function closeBookingModal() {
            document.getElementById('bookingModal').style.display = 'none';
        }

        function sendWhatsApp(e) {
            e.preventDefault();
            const name = document.getElementById('b_name').value;
            const hotel = document.getElementById('b_hotel').value;
            const checkin = document.getElementById('b_checkin').value;
            const checkout = document.getElementById('b_checkout').value;
            const persons = document.getElementById('b_persons').value;
            const roomType = document.getElementById('b_roomtype').value;

            const message = `*NEW BOOKING REQUEST* 🔔\n\n*Name:* ${name}\n*Hotel:* ${hotel}\n*Check-in:* ${checkin}\n*Check-out:* ${checkout}\n*Persons:* ${persons}\n*Type:* ${roomType}\n\n_Please confirm availability and let me know the advance amount._`;
            const whatsappUrl = `https://wa.me/917675962840?text=${encodeURIComponent(message)}`;
            
            window.open(whatsappUrl, '_blank');
            closeBookingModal();
        }

        window.onclick = function(event) {
            let modal = document.getElementById('bookingModal');
            if (event.target == modal) {
                closeBookingModal();
            }
        }
    </script>
</body>
</html>

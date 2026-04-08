<!DOCTYPE html>
<html>
<head>
    <title>Ahobilam Rooms</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background: #FFF8E1; /* This is your page background color */
        }

        /* NAVBAR */
        .navbar {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 10px 20px;
            background: #d6a65c;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            box-sizing: border-box; /* Fixes potential horizontal scroll */
        }

        /* LOGO */
        .logo {
            height: 80px; /* Adjusted slightly for better fit */
            width: 80px;
            object-fit: contain;
            background: transparent;
            display: block;
        }

        .site-title {
            margin: 0;
            color: white;
            font-size: 24px;
        }

        .menu a {
            margin-left: 20px;
            text-decoration: none;
            color: white;
            font-weight: bold;
        }

        /* FIX FOR WHITE SPACE / OVERLAP */
        header {
            margin-top: 100px; /* This pushes the content down so it starts AFTER the navbar */
            background: #FFCC80;
            color: white;
            padding: 60px 20px;
            text-align: center;
        }

        /* CONTENT SECTIONS */
        section {
            padding: 40px;
            text-align: center;
        }

        button {
            background: #27ae60;
            color: white;
            padding: 15px 25px;
            border: none;
            font-size: 18px;
            cursor: pointer;
            border-radius: 5px;
        }

        .complex-card {
            width: 320px;
            margin: 40px auto; /* Centered the card */
            text-align: center;
        }

        .complex-photo {
            width: 100%;
            max-width: 300px;
            border-radius: 12px;
            display: block;
            margin: 0 auto 15px auto;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
        }

        .complex-btn {
            background: #27ae60;
            color: white;
            padding: 20px;
            border: none;
            font-size: 22px;
            border-radius: 20px;
            cursor: pointer;
            width: 100%;
        }
    </style>
</head>
<body>

    <!-- NAVBAR -->
    <div class="navbar">
        <img src="AVS1.png" class="logo" alt="Logo">
        <h1 class="site-title">Ahobilam</h1>
        <img src="without_bg.png" class="logo" alt="Logo">
        <div class="menu">
            <a href="#about">About</a>
            <a href="#hotels">Hotels</a>
            <a href="#temple">Temple</a>
        </div>
    </div>

    <!-- HEADER: Starts below the fixed navbar -->
    <header id="about">
        <h1>Ahobilam Rooms</h1>
        <p>
            <strong>Welcome to Ahobilam Rooms</strong><br>
            Your ideal accommodation near the sacred Ahobilam Temple.
        </p>
    </header>

    <section>
        <h2>Our Services</h2>
        <p>
            ✅ AC & Non-AC Rooms<br>
            ✅ Hot Water 24 Hours<br>
            ✅ Parking Available<br>
            ✅ Family Friendly
        </p>
        <button onclick="location.href='tel:+917675962840'">
            Call For Booking
        </button>
    </section>

    <!-- HOTEL CARD -->
    <div class="complex-card" id="hotels">
        <img src="Rajeshwari.Complex.jpeg" class="complex-photo" alt="Hotel Photo">
        <button class="complex-btn" onclick="location.href='rooms.html'">
            Rajeshwari Complex<br>
            <strong>Book Now</strong>
        </button>
    </div>

</body>
</html>

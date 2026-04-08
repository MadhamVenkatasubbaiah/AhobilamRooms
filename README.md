<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahobilam Rooms</title>
    <style>
        /* 1. GENERAL SETTINGS & WATERMARK */
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            margin: 0;
            background: #FFF8E1;
            /* Watermark Sketch Effect */
            background-image: url('AVS1.png'); 
            background-repeat: no-repeat;
            background-position: center;
            background-attachment: fixed;
            background-size: 50%;
            transition: 0.3s;
        }

        /* Create the "faded" watermark look over the background */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(255, 248, 225, 0.85); /* Adjust opacity here */
            z-index: -1;
        }

        /* 2. NAVIGATION BAR */
        .navbar {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 5px 20px;
            background: #d6a65c;
            position: fixed;
            top: 0; width: 100%;
            z-index: 2000;
            box-sizing: border-box;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .logo-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        /* ADJUST LOGO SIZE HERE */
        .logo {
            height: 60px; /* Smaller, cleaner size */
            width: auto;
            object-fit: contain;
        }

        .site-title {
            color: white;
            margin: 0;
            font-size: 1.5rem;
        }

        /* 3. MENU (DESKTOP) */
        .menu {
            display: flex;
        }

        .menu a {
            margin-left: 20px;
            text-decoration: none;
            color: white;
            font-weight: bold;
            font-size: 16px;
        }

        /* 4. MOBILE MENU (HIDDEN BY DEFAULT) */
        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
        }

        .menu-toggle span {
            height: 3px;
            width: 25px;
            background: white;
            margin: 4px 0;
            border-radius: 2px;
        }

        /* 5. CONTENT ADJUSTMENT (Prevents "test data" overlap) */
        header {
            margin-top: 80px; /* Pushes content below the fixed navbar */
            background: #FFCC80;
            color: white;
            padding: 60px 20px;
            text-align: center;
            width: 80%; /* Match your sketch look */
            margin-left: auto;
            margin-right: auto;
            border-radius: 8px;
        }

        /* 6. RESPONSIVE DESIGN (MOBILE) */
        @media (max-width: 768px) {
            .menu {
                display: none; /* Hide standard menu */
                flex-direction: column;
                position: absolute;
                top: 70px;
                right: 20px;
                background: #d6a65c;
                padding: 20px;
                border-radius: 10px;
                width: 150px;
            }

            .menu.active {
                display: flex; /* Show when toggled */
            }

            .menu a {
                margin: 10px 0;
            }

            .menu-toggle {
                display: flex; /* Show hamburger on mobile */
            }

            .site-title { font-size: 1.2rem; }
            .logo { height: 45px; }
            header { width: 95%; margin-top: 100px; }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="logo-container">
            <img src="AVS1.png" class="logo" alt="Logo 1">
            <h1 class="site-title">Ahobilam112313</h1>
            <img src="without_bg.png" class="logo" alt="Logo 2">
        </div>

        <!-- Hamburger Icon for Mobile -->
        <div class="menu-toggle" onclick="toggleMenu()">
            <span></span>
            <span></span>
            <span></span>
        </div>

        <div class="menu" id="navLinks">
            <a href="#about">About</a>
            <a href="#hotels">Hotels</a>
            <a href="#temple">Temple</a>
        </div>
    </nav>

    <header id="about">
        <h1>Ahobilam Rooms</h1>
        <p>Welcome to Ahobilam Rooms<br>
        Your ideal accommodation near the sacred Ahobilam Temple.</p>
    </header>

    <!-- MOBILE MENU SCRIPT -->
    <script>
        function toggleMenu() {
            const nav = document.getElementById('navLinks');
            nav.classList.toggle('active');
        }
    </script>

</body>
</html>

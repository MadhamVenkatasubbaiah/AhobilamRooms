<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>

/* ===== GLOBAL ===== */
body{
    margin:0;
    font-family: 'Segoe UI', sans-serif;
    background:#0b0b0b;
    color:white;
}

h1,h2,h3{
    font-family: Georgia, serif;
}

.gold{
    color:#d4af37;
}

/* ===== NAVBAR ===== */
.navbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:15px 40px;
    background:#000;
    border-bottom:1px solid rgba(255,255,255,0.1);
    position:fixed;
    width:100%;
    z-index:1000;
}

.logo{
    display:flex;
    align-items:center;
    gap:10px;
}

.logo img{
    height:40px;
}

.logo-text{
    color:#d4af37;
}

.nav-links{
    display:flex;
    gap:30px;
    align-items:center;
}

.nav-links a{
    color:#ccc;
    text-decoration:none;
    font-weight:500;
}

.nav-links a:hover{
    color:#d4af37;
}

.book-btn{
    background:#d4af37;
    color:black;
    padding:10px 20px;
    border-radius:8px;
    font-weight:bold;
}

/* ===== HERO ===== */
.hero{
    height:100vh;
    background:url('room.jpg') center/cover no-repeat;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    position:relative;
}

.hero::after{
    content:"";
    position:absolute;
    width:100%;
    height:100%;
    background:rgba(0,0,0,0.6);
}

.hero-content{
    position:relative;
    z-index:1;
}

.hero h1{
    font-size:70px;
    color:#d4af37;
    margin:10px 0;
}

.hero p{
    color:#ccc;
}

.hero-buttons{
    margin-top:20px;
}

.hero-buttons button{
    padding:12px 25px;
    margin:10px;
    border-radius:8px;
    border:none;
    cursor:pointer;
}

.btn-primary{
    background:#d4af37;
    color:black;
}

.btn-outline{
    background:transparent;
    border:1px solid #d4af37;
    color:#d4af37;
}

/* ===== AMENITIES ===== */
.section{
    padding:80px 40px;
    text-align:center;
}

.cards{
    display:flex;
    justify-content:center;
    gap:20px;
    flex-wrap:wrap;
    margin-top:40px;
}

.card{
    background:#111;
    border:1px solid rgba(255,255,255,0.1);
    padding:30px;
    width:250px;
    border-radius:12px;
}

.card h3{
    color:#d4af37;
}

/* ===== ROOMS ===== */
.room-container{
    display:flex;
    justify-content:center;
    gap:40px;
    flex-wrap:wrap;
}

.room-card{
    background:#111;
    border-radius:12px;
    overflow:hidden;
    width:400px;
}

.room-card img{
    width:100%;
}

.room-content{
    padding:20px;
    text-align:left;
}

.tags span{
    background:#222;
    padding:5px 10px;
    margin-right:5px;
    border-radius:5px;
    font-size:12px;
}

.room-content button{
    margin-top:15px;
    background:#d4af37;
    border:none;
    padding:10px 15px;
    border-radius:6px;
}

/* ===== DISCOVER ===== */
.discover{
    display:flex;
    align-items:center;
    gap:50px;
    padding:80px;
}

.discover img{
    width:500px;
    border-radius:12px;
}

.discover-text{
    max-width:500px;
}

/* ===== FLOAT ===== */
.whatsapp{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#25D366;
    color:white;
    width:60px;
    height:60px;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:24px;
}

/* ===== MOBILE ===== */
@media(max-width:768px){
.hero h1{font-size:40px;}
.discover{flex-direction:column;}
}

</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">
    <div class="logo">
        <img src="logo.png">
        <div class="logo-text">
            <b>Madam Rajeswari</b><br>
            <small>COMPLEX</small>
        </div>
    </div>

    <div class="nav-links">
        <a href="#">Home</a>
        <a href="#">Rooms</a>
        <a href="#">Temple History</a>
        <a href="#">Contact</a>
        <a class="book-btn" href="tel:+917675962840">📞 Book Now</a>
    </div>
</div>

<!-- HERO -->
<div class="hero">
    <div class="hero-content">
        <p class="gold">WELCOME TO</p>
        <h1>Madam Rajeswari<br>Complex</h1>
        <p>Ahobilam, Andhra Pradesh</p>
        <p>Your divine stay near the sacred Narasimha temples</p>

        <div class="hero-buttons">
            <button class="btn-primary">Book via WhatsApp</button>
            <button class="btn-outline">View Rooms</button>
        </div>
    </div>
</div>

<!-- AMENITIES -->
<div class="section">
    <h2 class="gold">Our Amenities</h2>

    <div class="cards">
        <div class="card">
            <h3>Air Conditioned</h3>
            <p>All rooms are fully air conditioned</p>
        </div>

        <div class="card">
            <h3>King Size Beds</h3>
            <p>Premium comfort beds</p>
        </div>

        <div class="card">
            <h3>Free Wi-Fi</h3>
            <p>High speed internet</p>
        </div>

        <div class="card">
            <h3>24/7 Security</h3>
            <p>Round the clock service</p>
        </div>
    </div>
</div>

<!-- ROOMS -->
<div class="section">
    <h2 class="gold">Our Rooms</h2>

    <div class="room-container">

        <div class="room-card">
            <img src="room1.jpg">
            <div class="room-content">
                <h3>King AC Room – 2 Sharing</h3>
                <p>Perfect for couples</p>

                <div class="tags">
                    <span>AC</span>
                    <span>King Bed</span>
                    <span>WiFi</span>
                    <span>TV</span>
                </div>

                <button>Book Now</button>
            </div>
        </div>

        <div class="room-card">
            <img src="room2.jpg">
            <div class="room-content">
                <h3>King AC Room – 3 Sharing</h3>
                <p>Ideal for family</p>

                <div class="tags">
                    <span>AC</span>
                    <span>King Bed</span>
                    <span>WiFi</span>
                    <span>TV</span>
                </div>

                <button>Book Now</button>
            </div>
        </div>

    </div>
</div>

<!-- DISCOVER -->
<div class="discover">
    <div class="discover-text">
        <p class="gold">DISCOVER</p>
        <h2 class="gold">Ahobilam – The Sacred Abode</h2>

        <p>
        Ahobilam is a renowned pilgrimage centre in Andhra Pradesh,
        famous for the nine temples of Lord Narasimha.
        </p>

        <p>
        Our hotel is located near the temple, making it perfect for your stay.
        </p>
    </div>

    <img src="temple.jpg">
</div>

<!-- FLOAT -->
<a class="whatsapp" href="https://wa.me/917675962840">💬</a>

</body>
</html>

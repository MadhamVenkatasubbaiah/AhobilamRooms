<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>

/* ================= GLOBAL ================= */
body{
    margin:0;
    font-family: 'Segoe UI', sans-serif;
    background:#0b0b0b;
    color:#fff;
}

h1,h2,h3{
    color:#d4af37;
}

/* ================= NAVBAR ================= */
.navbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:15px 40px;
    background:#000;
    position:fixed;
    width:100%;
    top:0;
    z-index:1000;
}

.logo{
    color:#d4af37;
    font-size:22px;
    font-weight:bold;
}

.menu{
    display:flex;
    gap:30px;
    align-items:center;
}

.menu a{
    color:#d4af37;
    text-decoration:none;
    font-weight:500;
}

.book-btn{
    background:#d4af37;
    color:black;
    padding:10px 18px;
    border-radius:8px;
    font-weight:bold;
}

/* ================= HERO ================= */
.hero{
    height:100vh;
    background:url("room.jpg") center/cover no-repeat;
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
    z-index:2;
}

.hero h1{
    font-size:60px;
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
    font-weight:bold;
}

.whatsapp-btn{
    background:#d4af37;
}

.view-btn{
    background:transparent;
    border:1px solid #d4af37;
    color:#d4af37;
}

/* ================= AMENITIES ================= */
.section{
    padding:80px 40px;
    text-align:center;
}

.amenities{
    display:flex;
    gap:20px;
    flex-wrap:wrap;
    justify-content:center;
}

.card{
    border:1px solid #333;
    padding:25px;
    border-radius:12px;
    width:220px;
}

/* ================= ROOMS ================= */
.rooms{
    display:flex;
    gap:30px;
    flex-wrap:wrap;
    justify-content:center;
}

.room-card{
    width:320px;
    border-radius:12px;
    overflow:hidden;
    background:#111;
}

.room-card img{
    width:100%;
}

.room-content{
    padding:20px;
    text-align:left;
}

.room-content button{
    background:#d4af37;
    border:none;
    padding:10px;
    border-radius:6px;
    margin-top:10px;
}

/* ================= FLOAT ================= */
.whatsapp{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#25D366;
    width:60px;
    height:60px;
    border-radius:50%;
    display:flex;
    justify-content:center;
    align-items:center;
    font-size:25px;
}

/* ================= MOBILE ================= */
@media(max-width:768px){
.hero h1{ font-size:35px; }
.menu{ display:none; }
}

</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">
<div class="logo">Madam Rajeswari</div>

<div class="menu">
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
<p>WELCOME TO</p>
<h1>Madam Rajeswari Complex</h1>
<p>Ahobilam, Andhra Pradesh</p>
<p>Your divine stay near Narasimha temples</p>

<div class="hero-buttons">
<button class="whatsapp-btn">Book via WhatsApp</button>
<button class="view-btn">View Rooms</button>
</div>
</div>
</div>

<!-- AMENITIES -->
<div class="section">
<h2>Our Amenities</h2>

<div class="amenities">
<div class="card">Air Conditioned</div>
<div class="card">King Size Beds</div>
<div class="card">Free Wi-Fi</div>
<div class="card">24/7 Security</div>
</div>
</div>

<!-- ROOMS -->
<div class="section">
<h2>Our Rooms</h2>

<div class="rooms">

<div class="room-card">
<img src="room.jpg">
<div class="room-content">
<h3>King AC Room – 2 Sharing</h3>
<p>Perfect for couples</p>
<button>Book Now</button>
</div>
</div>

<div class="room-card">
<img src="room.jpg">
<div class="room-content">
<h3>King AC Room – 3 Sharing</h3>
<p>Ideal for family</p>
<button>Book Now</button>
</div>
</div>

</div>
</div>

<!-- FLOAT -->
<div class="whatsapp">💬</div>

</body>
</html>

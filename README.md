<html>
<head>

<style>

/* ================= BODY ================= */
body{
    font-family: Arial;
    margin:0;
    background:#FFE0B2;
}

/* ================= NAVBAR ================= */
.navbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    background:#FF9933;
    height:80px;
    padding:0 10px;
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    box-sizing:border-box;
}

.left img{ height:40px; }
.right img{ height:40px; }

.center{
    flex:1;
    text-align:center;
    position:relative;
}

.center h1{
    margin:0;
    color:white;
    font-size:20px;
}

/* MENU */
.menu{
    display:flex;
    justify-content:center;
    gap:12px;
}

.menu a{
    color:white;
    text-decoration:none;
    font-weight:bold;
    font-size:13px;
    cursor:pointer;
}

/* DROPDOWN */
.dropdown{
    position:relative;
}

.dropdown-content{
    display:none;
    position:absolute;
    top:25px;
    left:0;
    background:#fff;
    min-width:250px;
    border-radius:5px;
    padding:10px;
    box-shadow:0 4px 10px rgba(0,0,0,0.2);
    text-align:left;
}

.dropdown:hover .dropdown-content{
    display:block;
}

/* MOBILE */
.menu-toggle{
    display:none;
    font-size:26px;
    color:white;
    cursor:pointer;
}

@media(max-width:768px){

.menu{
    display:none;
    flex-direction:column;
    position:fixed;
    top:80px;
    left:0;
    width:100%;
    background:#d6a65c;
}

.menu.show{ display:flex; }

.menu-toggle{
    display:block;
    position:absolute;
    right:10px;
    top:5px;
}

.right img{ display:none; }

.dropdown-content{
    position:static;
    box-shadow:none;
}
}

/* ================= HEADER ================= */
header{
    margin-top:80px;
    padding:80px 20px;
    text-align:center;
    color:black;
    background:#FFE0B2;
    position:relative;
}

header::before{
    content:"";
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    width:600px;
    height:600px;
    background:url("without_bg.png") no-repeat center;
    background-size:contain;
    opacity:0.15;
}

/* ================= CONTENT ================= */
section{
    padding:40px;
    text-align:center;
}

button{
    background:#27ae60;
    color:white;
    padding:12px 20px;
    border:none;
    border-radius:5px;
    cursor:pointer;
}

/* ================= COMPLEX ================= */
.complex-container{
    display:flex;
    justify-content:center;
    gap:30px;
    flex-wrap:wrap;
}

.complex-card{
    text-align:center;
}

.complex-photo{
    width:280px;
    border-radius:10px;
}

/* ================= PANEL ================= */
.panel{
    display:none;
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    background:#FFE0B2;
    z-index:2000;
    padding:20px;
    overflow:auto;
}

/* ================= ROOMS ================= */
.room-row{
    display:flex;
    align-items:center;
    gap:20px;
    background:white;
    margin:20px;
    padding:15px;
    border-radius:10px;
}

.room-main{
    width:200px;
    border-radius:10px;
    cursor:pointer;
}

.room-info{
    text-align:left;
}

.gallery{
    display:none;
}

.gallery img{
    width:150px;
    margin:10px;
    border-radius:10px;
}

/* ================= FLOAT ================= */
.whatsapp{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#25D366;
    color:white;
    width:60px;
    height:60px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:26px;
    border-radius:50%;
    z-index:3000;
}

.call{
    position:fixed;
    bottom:90px;
    right:20px;
    background:#007bff;
    color:white;
    width:60px;
    height:60px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:22px;
    border-radius:50%;
    z-index:3000;
}

</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">

<div class="left">
<img src="logo.png">
</div>

<div class="center">
<h1>AHOBILAM</h1>

<span class="menu-toggle" onclick="toggleMenu()">☰</span>

<div class="menu" id="menu">

<div class="dropdown">
<a>About ▾</a>
<div class="dropdown-content">
According to legend, when the Devas witnessed the awe-inspiring form of Lord Vishnu as Narasimha, a fusion of great strength (“Ahobala”) and the divine cave (“Ahobila”), they exclaimed in awe. This led to the name Ahobilam.
</div>
</div>

<div class="dropdown">
<a>Hotels ▾</a>
<div class="dropdown-content">
Hotel 1<br>Hotel 2<br>Hotel 3
</div>
</div>

<div class="dropdown">
<a>Temple Timings ▾</a>
<div class="dropdown-content">
Morning: 6:00 AM – 1:00 PM<br>
Evening: 3:00 PM – 8:30 PM
</div>
</div>

</div>
</div>

<div class="right">
<img src="AVS3.png">
</div>

</div>

<!-- HEADER -->
<header>
<h1>Ahobilam Rooms</h1>
<p>Providing the best accommodation near temple</p>
</header>

<!-- CONTENT -->
<section>

<h2>Facilities</h2>

<p>
🛏 AC & Non-AC Rooms<br>
🚿 Hot Water 24 Hours<br>
🚘 Parking Available<br>
👨‍👩‍👦 Family Friendly
</p>

<button onclick="location.href='tel:+917675962840'">
Call For Booking
</button>

</section>

<!-- COMPLEX -->
<div class="complex-container">

<div class="complex-card">
<img src="Rajeshwari.Complex.jpeg" class="complex-photo"><br><br>
<button onclick="openPanel('rooms1')">
Rajeshwari Complex - Book Now
</button>
</div>

<div class="complex-card">
<img src="Rajeshwari.Complex.jpeg" class="complex-photo"><br><br>
<button onclick="openPanel('rooms2')">
Veerabadhra Complex - Book Now
</button>
</div>

</div>

<!-- PANEL 1 -->
<div id="rooms1" class="panel">
<button onclick="goHome()">⬅ Back</button>

<h2>Rajeshwari Rooms</h2>

<div class="room-row">
<img src="3bed.jpeg" class="room-main" onclick="toggleGallery('g1a')">
<div class="room-info">
<h3>3 Bed Room</h3>
<button onclick="location.href='tel:+917675962840'">Book ₹1600</button>
</div>
</div>

<div id="g1a" class="gallery">
<img src="3bed.jpeg">
<img src="washroom.jpeg">
</div>

<div class="room-row">
<img src="2-bed.jpeg" class="room-main" onclick="toggleGallery('g2a')">
<div class="room-info">
<h3>2 Bed Room</h3>
<button onclick="location.href='tel:+917675962840'">Book ₹1200</button>
</div>
</div>

<div id="g2a" class="gallery">
<img src="2-bed.jpeg">
</div>

</div>

<!-- PANEL 2 -->
<div id="rooms2" class="panel">
<button onclick="goHome()">⬅ Back</button>

<h2>Veerabadhra Rooms</h2>

<div class="room-row">
<img src="3bed.jpeg" class="room-main" onclick="toggleGallery('g1b')">
<div class="room-info">
<h3>3 Bed Room</h3>
<button onclick="location.href='tel:+917675962840'">Book ₹1600</button>
</div>
</div>

<div id="g1b" class="gallery">
<img src="3bed.jpeg">
<img src="washroom.jpeg">
</div>

<div class="room-row">
<img src="2-bed.jpeg" class="room-main" onclick="toggleGallery('g2b')">
<div class="room-info">
<h3>2 Bed Room</h3>
<button onclick="location.href='tel:+917675962840'">Book ₹1200</button>
</div>
</div>

<div id="g2b" class="gallery">
<img src="2-bed.jpeg">
</div>

</div>

<!-- FLOAT -->
<a class="whatsapp" href="https://wa.me/917675962840">💬</a>
<a class="call" href="tel:+917675962840">📞</a>

<script>

function toggleMenu(){
document.getElementById("menu").classList.toggle("show");
}

function openPanel(id){
document.getElementById(id).style.display="block";
}

function goHome(){
document.querySelectorAll(".panel").forEach(p=>p.style.display="none");
}

function toggleGallery(id){
let g=document.getElementById(id);
g.style.display = (g.style.display==="block") ? "none":"block";
}

</script>

</body>
</html>

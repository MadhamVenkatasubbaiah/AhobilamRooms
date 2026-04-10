<!DOCTYPE html>
<html>
<head>

<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ahobilam Rooms</title>

<style>

/* ===== BODY ===== */
body{
    font-family: Arial;
    margin:0;
    background:#FFF8E1;
}

/* ===== NAVBAR ===== */
.navbar {
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: center;
    background: #FF9933;
    height: 100px;
    padding: 0 20px;
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 1000;
}

/* Center */
.center {
    text-align: center;
}

.center h1 {
    margin: 0;
    color: white;
}

/* MENU */
.menu {
    display: flex;
    justify-content: center;
    gap: 30px;
}

.menu a {
    color: white;
    text-decoration: none;
}

/* RIGHT SIDE */
.right{
    display:flex;
    align-items:center;
    gap:10px;
}

.menu-toggle{
    display:none;
    font-size:28px;
    color:white;
    cursor:pointer;
}

/* MOBILE */
@media(max-width:768px){
.menu{
    display:none;
    flex-direction:column;
    position:fixed;
    top:100px;
    left:0;
    background:#d6a65c;
    width:100%;
}
.menu.show{
    display:flex;
}
.menu-toggle{
    display:block;
}
}

/* HEADER */
header{
    margin-top:100px;
    padding:90px 20px;
    text-align:center;
    background:#e8b97a;
    color:white;
}

/* CONTENT */
section{
    padding:40px;
    text-align:center;
}

/* BUTTON */
button{
    background:#27ae60;
    color:white;
    padding:15px 25px;
    border:none;
    cursor:pointer;
    border-radius:5px;
}

/* CARD */
.complex-card{
    width:320px;
    margin:40px auto;
    text-align:center;
}

.complex-photo{
    width:300px;
    border-radius:12px;
}

.complex-btn{
    margin-top:15px;
}

/* ===== PANELS ===== */
.panel{
    display:none;
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    background:#FFF8E1;
    z-index:2000;
    padding:20px;
    overflow:auto;
}

/* ===== ROOMS DESIGN ===== */
.rooms-container{
display:flex;
justify-content:center;
gap:30px;
flex-wrap:wrap;
padding:40px;
}

.room-card{
background:white;
border-radius:10px;
box-shadow:0 4px 10px rgba(0,0,0,0.2);
width:300px;
padding:15px;
}

.room-card img{
width:100%;
border-radius:10px;
}

.book-btn{
background:#27ae60;
color:white;
padding:10px 20px;
border:none;
border-radius:5px;
cursor:pointer;
margin-top:10px;
}

/* WhatsApp */
.whatsapp{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#25D366;
    color:white;
    padding:14px;
    border-radius:50px;
}

</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">

<div>
<img src="logo.png" height="70">
</div>

<div class="center">
<h1>AHOBILAM</h1>

<div class="menu" id="menu">
<a href="#" onclick="openPanel('aboutPanel')">About</a>
<a href="#" onclick="openPanel('hotelsPanel')">Hotels</a>
<a href="#" onclick="openPanel('timingsPanel')">Temple Timings</a>
</div>
</div>

<div class="right">
<span class="menu-toggle" onclick="toggleMenu()">☰</span>
<img src="AVS3.png" height="70">
</div>

</div>

<!-- HEADER -->
<header>
<h1>Ahobilam Rooms</h1>
<p>Welcome to Ahobilam Rooms</p>
</header>

<!-- CONTENT -->
<section>
<h2>Facilities</h2>
<p>AC & Non-AC Rooms | Hot Water | Parking | Family Friendly</p>

<button onclick="location.href='tel:+917675962840'">
Call For Booking
</button>
</section>

<!-- ROOM CARD -->
<div class="complex-card">
<img src="Rajeshwari.Complex.jpeg" class="complex-photo">
<button class="complex-btn" onclick="openPanel('roomsPanel')">
Rajeshwari Complex<br>Book Now
</button>
</div>

<!-- ===== ROOMS PANEL ===== -->
<div id="roomsPanel" class="panel">

<button onclick="goHome()">⬅ Back</button>

<h1>Rajeshwari Complex</h1>

<div class="rooms-container">

<div class="room-card">
<img src="3bed.jpeg">
<img src="washroom.jpeg">
<h3>3 Bed Room</h3>
<p>AC + WiFi</p>
<button class="book-btn" onclick="location.href='tel:+917675962840'">
Book Now - ₹1600
</button>
</div>

<div class="room-card">
<img src="2-bed.jpeg">
<h3>2 Bed Room</h3>
<p>AC + WiFi</p>
<button class="book-btn" onclick="location.href='tel:+917675962840'">
Book Now - ₹1200
</button>
</div>

</div>
</div>

<!-- OTHER PANELS -->
<div id="aboutPanel" class="panel">
<button onclick="goHome()">⬅ Back</button>
<h2>About</h2>
<p>Best stay near temple.</p>
</div>

<div id="hotelsPanel" class="panel">
<button onclick="goHome()">⬅ Back</button>
<h2>Hotels</h2>
<p>Coming soon</p>
</div>

<div id="timingsPanel" class="panel">
<button onclick="goHome()">⬅ Back</button>
<h2>Temple Timings</h2>
<p>7AM - 5PM</p>
</div>

<!-- WhatsApp -->
<a class="whatsapp"
href="https://wa.me/917675962840?text=Hi%20I%20want%20room"
target="_blank">💬</a>

<script>

function toggleMenu(){
document.getElementById("menu").classList.toggle("show");
}

function openPanel(id){
document.getElementById(id).style.display="block";
}

function goHome(){
let panels=document.querySelectorAll(".panel");
panels.forEach(p=>p.style.display="none");
}

</script>

</body>
</html>

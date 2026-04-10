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
    left: 0;
    width: 100%;
    z-index: 1000;

    box-sizing: border-box;
}

/* Center */
.center {
    text-align: center;
}

.center h1 {
    margin: 0;
    color: white;
    font-size: 32px;
    font-weight: bold;
}

/* MENU */
.menu {
    display: flex;
    justify-content: center;
    gap: 30px;
    margin-top: 5px;
}

.menu a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

/* RIGHT SIDE */
.right{
    display:flex;
    align-items:center;
    gap:10px;
}

/* HAMBURGER */
.menu-toggle{
    display:none;
    font-size:28px;
    color:white;
    cursor:pointer;
}

/* ===== MOBILE VIEW ===== */
@media(max-width:768px){

.menu{
    display:none;
    flex-direction:column;
    position:fixed;
    top:100px;
    left:0;
    background:#d6a65c;
    width:100%;
    text-align:center;
}

.menu a{
    padding:15px;
    border-top:1px solid rgba(255,255,255,0.3);
}

.menu.show{
    display:flex;
}

.menu-toggle{
    display:block;
}

.right img{
    display:none;
}

.center h1{
    font-size:24px;
}
}

/* ===== HEADER ===== */
header{
    margin-top:100px;
    padding:90px 20px;
    text-align:center;
    color:white;
    position:relative;
    background:#e8b97a;
    overflow:hidden;
}

header::before{
    content:"";
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    width:300px;
    height:300px;
    background:url("without_bg.png") no-repeat center;
    background-size:contain;
    opacity:0.08;
}

header h1,
header p{
    position:relative;
    z-index:2;
}

/* ===== CONTENT ===== */
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
    font-size:18px;
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
    box-shadow:0 4px 12px rgba(0,0,0,0.3);
}

.complex-btn{
    margin-top:15px;
    background:#27ae60;
    color:white;
    padding:18px;
    border:none;
    font-size:20px;
    border-radius:10px;
    cursor:pointer;
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

.panel button{
    background:#FF9933;
    color:white;
    border:none;
    padding:10px 15px;
    margin-bottom:20px;
    border-radius:5px;
    cursor:pointer;
}

/* ===== WHATSAPP BUTTON ===== */
.whatsapp{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#25D366;
    color:white;
    padding:14px 16px;
    border-radius:50px;
    text-decoration:none;
    font-size:18px;
    box-shadow:0 4px 10px rgba(0,0,0,0.3);
    z-index:3000;
}

</style>
</head>

<body>

<!-- ===== NAVBAR ===== -->
<div class="navbar">

  <div class="left">
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

<!-- ===== HEADER ===== -->
<header>
<h1>Ahobilam Rooms</h1>

<p>
<strong>Welcome to Ahobilam Rooms</strong><br>
Your ideal accommodation near the sacred Ahobilam Temple.
</p>
</header>

<!-- ===== CONTENT ===== -->
<section>

<h2>Facilities</h2>

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

<!-- ===== ROOM CARD 1 ===== -->
<div class="complex-card">

<img src="Rajeshwari.Complex.jpeg" class="complex-photo">

<button class="complex-btn"
onclick="location.href='rooms.html'">
Rajeshwari Complex<br>
Book Now
</button>

</div>

<!-- ===== ROOM CARD 2 ===== -->
<div class="complex-card">

<img src="Rajeshwari.Complex.jpeg" class="complex-photo">

<button class="complex-btn"
onclick="location.href='rooms.html'">
Rajeshwari Complex<br>
Book Now
</button>

</div>

<!-- ===== PANELS ===== -->

<div id="aboutPanel" class="panel">
  <button onclick="goHome()">⬅ Back</button>
  <h2>About</h2>
  <p>Welcome to Ahobilam Rooms. Best stay near temple.</p>
</div>

<div id="hotelsPanel" class="panel">
  <button onclick="goHome()">⬅ Back</button>
  <h2>Hotels</h2>
  <p>Nearby hotels list coming soon.</p>
</div>

<div id="timingsPanel" class="panel">
  <button onclick="goHome()">⬅ Back</button>
  <h2>Temple Timings</h2>
  <p>Morning: 7:00 AM – 1:00 PM</p>
  <p>Afternoon: 2:00 PM – 5:00 PM</p>
</div>

<!-- ===== WHATSAPP BUTTON (AUTO MESSAGE ADDED) ===== -->
<a class="whatsapp"
href="https://wa.me/917675962840?text=Hi%20I%20want%20to%20book%20a%20room%20at%20Ahobilam%20Rooms.%20Please%20share%20availability%20and%20price."
target="_blank">
💬
</a>

<!-- ===== SCRIPT ===== -->
<script>

function toggleMenu(){
    document.getElementById("menu").classList.toggle("show");
}

function openPanel(id){
    document.getElementById(id).style.display = "block";
}

function goHome(){
    document.getElementById("aboutPanel").style.display = "none";
    document.getElementById("hotelsPanel").style.display = "none";
    document.getElementById("timingsPanel").style.display = "none";
}

</script>

</body>
</html>

<!DOCTYPE html>
<html>
<head>

<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ahobilam Rooms</title>

<style>

/* BODY */
body{
    font-family: Arial;
    margin:0;
    background:#FFF8E1;
}

/* NAVBAR */
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
    z-index:1000;
}

.center{
    text-align:center;
}

.menu{
    display:flex;
    justify-content:center;
    gap:20px;
}

.menu a{
    color:white;
    text-decoration:none;
    font-weight:bold;
}

.right{
    display:flex;
    align-items:center;
    gap:10px;
}

/* MOBILE */
@media(max-width:768px){
    .right img{
        display:none;
    }
}

/* HEADER */
header{
    margin-top:100px;
    padding:90px 20px;
    text-align:center;
    color:white;
    background:#e8b97a;
    position:relative;
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

/* SECTION */
section{
    padding:40px;
    text-align:center;
}

/* BUTTON */
button{
    background:#27ae60;
    color:white;
    padding:12px 20px;
    border:none;
    border-radius:5px;
    cursor:pointer;
}

/* CARD */
.complex-card{
    text-align:center;
    margin:30px;
}

.complex-photo{
    width:300px;
    border-radius:10px;
}

/* PANEL */
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

/* ROOM ROW */
.room-row{
    display:flex;
    align-items:center;
    gap:20px;
    background:white;
    margin:20px;
    padding:15px;
    border-radius:10px;
    box-shadow:0 4px 10px rgba(0,0,0,0.2);
}

.room-main{
    width:220px;
    border-radius:10px;
    cursor:pointer;
}

.room-info{
    text-align:left;
}

/* GALLERY */
.gallery{
    display:none;
    margin-left:20px;
}

.gallery img{
    width:180px;
    margin:10px;
    border-radius:10px;
}

/* WHATSAPP */
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
<h2 style="color:white;margin:0;">AHOBILAM</h2>

<div class="menu">
<a href="#" onclick="openPanel('aboutPanel')">About</a>
<a href="#" onclick="openPanel('hotelsPanel')">Hotels</a>
<a href="#" onclick="openPanel('timingsPanel')">Temple Timings</a>
</div>

</div>

<div class="right">
<img src="AVS3.png" height="70">
</div>

</div>

<!-- HEADER -->
<header>
<h1>Ahobilam Rooms</h1>
<p>
<strong>Welcome to Ahobilam Rooms</strong><br>
Your ideal accommodation near the sacred temple
</p>
</header>

<!-- FACILITIES -->
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
<div class="complex-card">
<img src="Rajeshwari.Complex.jpeg" class="complex-photo">
<br><br>
<button onclick="openPanel('roomsPanel')">
Rajeshwari Complex - Book Now
</button>
</div>

<!-- ROOMS PANEL -->
<div id="roomsPanel" class="panel">

<button onclick="goHome()">⬅ Back</button>

<h2>Rajeshwari Complex</h2>

<!-- 3 BED -->
<div>
<div class="room-row">

<img src="3bed.jpeg" class="room-main"
onclick="toggleGallery('g1')">

<div class="room-info">
<h3>3 Bed Room</h3>
<p>AC + WiFi</p>
<button onclick="location.href='tel:+917675962840'">
Book ₹1600
</button>
</div>

</div>

<div id="g1" class="gallery">
<img src="3bed.jpeg">
<img src="washroom.jpeg">
</div>
</div>

<!-- 2 BED -->
<div>
<div class="room-row">

<img src="2-bed.jpeg" class="room-main"
onclick="toggleGallery('g2')">

<div class="room-info">
<h3>2 Bed Room</h3>
<p>AC + WiFi</p>
<button onclick="location.href='tel:+917675962840'">
Book ₹1200
</button>
</div>

</div>

<div id="g2" class="gallery">
<img src="2-bed.jpeg">
</div>
</div>

</div>

<!-- PANELS -->
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
<h2>Temple Timings1</h2>
<p>Morning: 7AM - 1PM<br>Afternoon: 2PM - 5PM</p>
</div>

<!-- WHATSAPP -->
<a class="whatsapp"
href="https://wa.me/917675962840?text=Hi%20I%20want%20room"
target="_blank">💬</a>

<script>

function openPanel(id){
document.getElementById(id).style.display="block";
}

function goHome(){
document.querySelectorAll(".panel")
.forEach(p=>p.style.display="none");
}

function toggleGallery(id){
let g=document.getElementById(id);
g.style.display = (g.style.display==="block") ? "none":"block";
}

</script>

</body>
</html>

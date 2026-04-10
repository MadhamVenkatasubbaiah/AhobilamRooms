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
}

/* HEADER WITH WATERMARK */
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
    border-radius:5px;
}

/* ROOM CARD */
.complex-card{
    width:320px;
    margin:40px auto;
    text-align:center;
}

.complex-photo{
    width:300px;
    border-radius:12px;
}

/* PANELS */
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

/* ROOMS */
.rooms-container{
    display:flex;
    justify-content:center;
    padding:20px;
}

/* ROOM ROW (IMAGE LEFT, BOOK RIGHT) */
.room-row{
    display:flex;
    align-items:center;
    gap:20px;
    background:white;
    padding:15px;
    border-radius:10px;
    box-shadow:0 4px 10px rgba(0,0,0,0.2);
}

/* MAIN IMAGE */
.room-main{
    width:250px;
    border-radius:10px;
    cursor:pointer;
}

/* RIGHT SIDE BOOK */
.room-info{
    text-align:left;
}

/* HIDDEN GALLERY */
.gallery{
    display:none;
    margin-top:20px;
}

.gallery img{
    width:200px;
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

<!-- HEADER -->
<header>
<h1>Ahobilam Rooms</h1>
<p>
<strong>Welcome to Ahobilam Rooms</strong><br>
Your ideal accommodation near temple
</p>
</header>

<!-- FACILITIES (RESTORED FULL) -->
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

<div class="rooms-container">

<!-- ROOM 1 -->
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

<!-- INSIDE PHOTOS -->
<div id="g1" class="gallery">
<img src="3bed.jpeg">
<img src="washroom.jpeg">
</div>
</div>

</div>

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

/* SHOW INSIDE PHOTOS */
function toggleGallery(id){
let g=document.getElementById(id);
g.style.display = (g.style.display==="block") ? "none":"block";
}

</script>

</body>
</html>

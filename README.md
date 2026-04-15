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

.left img{ height:90px; }
.right img{ height:90px; }

.center{
    flex:1;
    text-align:center;
    position:relative;
}

.center h1{
    margin:0;
    color:white;
    font-size:30px;
}

/* MENU */
.menu{
    display:flex;
    justify-content:center;
    gap:20px;
}

.menu a{
    color:white;
    text-decoration:none;
    font-weight:bold;
    font-size:18px;
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

/* GALLERY */
.gallery{
    display:none;
    margin-left:20px;
}

.gallery img{
    width:150px;
    margin:10px;
    border-radius:10px;
}

/* ===== SLIDER (ADDED) ===== */
.slider{
    display:none;
    margin-left:20px;
    position:relative;
}

.slide{ display:none; }

.slide img{
    width:200px;
    border-radius:10px;
}

.prev,.next{
    position:absolute;
    top:40%;
    padding:8px;
    background:rgba(0,0,0,0.5);
    color:white;
    cursor:pointer;
    border-radius:50%;
}

.prev{ left:0; }
.next{ right:0; }

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
<h1>AHOBILAM ROOMS</h1>

<span class="menu-toggle" onclick="toggleMenu()">☰</span>

<div class="menu" id="menu">

<div class="dropdown">
<a>About ▾</a>
<div class="dropdown-content">
Ahobilam sacred Narasimha temple location with 9 forms of Lord Narasimha.
</div>
</div>

<div class="dropdown">
<a>Hotels ▾</a>
<div class="dropdown-content">
<div onclick="openPanel('rooms1')" style="cursor:pointer;">Rajeshwari Complex</div>
<div onclick="openPanel('rooms2')" style="cursor:pointer;">Veerabadhra Complex</div>
</div>
</div>

<div class="dropdown">
<a>Temple Timings ▾</a>
<div class="dropdown-content">
Morning: 6AM–1PM<br>
Evening: 3PM–8:30PM
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
<p>Best rooms near temple</p>
</header>

<!-- FACILITIES -->
<section>
<h2>Facilities</h2>
🛏 AC Rooms<br>🚿 Hot Water<br>🚘 Parking
</section>

<!-- HOTELS -->
<section>
<h2>Our Hotels</h2>

<div class="complex-container">

<div class="complex-card">
<img src="Rajeshwari.Complex.jpeg" class="complex-photo"><br><br>
<button onclick="openPanel('rooms1')">Rajeshwari</button>
</div>

<div class="complex-card">
<img src="Rajeshwari.Complex.jpeg" class="complex-photo"><br><br>
<button onclick="openPanel('rooms2')">Veerabadhra</button>
</div>

</div>
</section>

<!-- MAP -->
<section>
<h2>Location</h2>
<iframe width="100%" height="300"
src="[https://www.google.com/maps?q=Ahobilam&output=embed](https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d710.4421127558048!2d78.67541071202811!3d15.131055112543342!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bb4f595d79cde9f%3A0xadc69bec3e67e13d!2sAhobilam%20Rajeshwari%20Complex!5e1!3m2!1sen!2sin!4v1776260115261!5m2!1sen!2sin)">
</iframe>
</section>

<!-- REVIEWS -->
<section>
<h2>Reviews ⭐</h2>
<div>⭐⭐⭐⭐⭐ Good rooms</div>
<div>⭐⭐⭐⭐ Nice stay</div>
</section>

<!-- PANEL 1 -->
<div id="rooms1" class="panel">
<button onclick="goHome()">⬅ Back</button>
<h2>Rajeshwari Rooms</h2>

<img src="3bed.jpeg" class="room-main" onclick="openSlider('s1')">

<div id="s1" class="slider">
<div class="slide"><img src="3bed.jpeg"></div>
<div class="slide"><img src="washroom.jpeg"></div>
<span class="prev" onclick="moveSlide('s1',-1)">❮</span>
<span class="next" onclick="moveSlide('s1',1)">❯</span>
</div>

</div>

<!-- PANEL 2 -->
<div id="rooms2" class="panel">
<button onclick="goHome()">⬅ Back</button>
<h2>Veerabadhra Rooms</h2>

<img src="3bed.jpeg" class="room-main" onclick="openSlider('s2')">

<div id="s2" class="slider">
<div class="slide"><img src="3bed.jpeg"></div>
<div class="slide"><img src="washroom.jpeg"></div>
<span class="prev" onclick="moveSlide('s2',-1)">❮</span>
<span class="next" onclick="moveSlide('s2',1)">❯</span>
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

/* SLIDER */
let slideIndex={};

function openSlider(id){
document.getElementById(id).style.display="block";
slideIndex[id]=0;
showSlide(id,0);
}

function moveSlide(id,n){
slideIndex[id]+=n;
showSlide(id,slideIndex[id]);
}

function showSlide(id,n){
let slides=document.querySelectorAll("#"+id+" .slide");
if(n>=slides.length){slideIndex[id]=0;}
if(n<0){slideIndex[id]=slides.length-1;}
slides.forEach(s=>s.style.display="none");
slides[slideIndex[id]].style.display="block";
}

</script>

</body>
</html>

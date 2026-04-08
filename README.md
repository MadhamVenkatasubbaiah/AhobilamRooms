<html>
<head>
<title>Ahobilam Rooms</title>

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>

/* ===== BODY ===== */
body{
    margin:0;
    font-family:Arial;
    background:#FFF8E1;
}

/* ===== NAVBAR ===== */
.navbar{
    display:flex;
    align-items:center;
    justify-content:space-between;
    background:#d6a65c;
    padding:6px 15px;   /* SMALL HEIGHT */
    position:fixed;
    top:0;
    width:100%;
    z-index:1000;
    box-sizing:border-box;
}

/* LOGO SIZE FIX */
.logo{
    height:45px;     /* CONTROL SIZE HERE */
    width:auto;
}

/* TITLE */
.site-title{
    color:white;
    margin:0;
    font-size:26px;
    flex:1;
    text-align:center;
}

/* MENU */
.menu{
    display:flex;
    gap:20px;
}

.menu a{
    text-decoration:none;
    color:white;
    font-weight:bold;
}

/* MOBILE MENU ICON */
.menu-icon{
    display:none;
    font-size:26px;
    color:white;
    cursor:pointer;
}

/* ===== HEADER ===== */
header{
    margin-top:70px; /* MATCH NAVBAR HEIGHT */
    background:#e6b56b;
    color:white;
    padding:70px 20px;
    text-align:center;
    position:relative;
    overflow:hidden;
}

/* WATERMARK */
header::before{
    content:"";
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    width:250px;
    height:250px;
    background:url("without_bg.png") no-repeat center;
    background-size:contain;
    opacity:0.12;
}

header *{
    position:relative;
    z-index:2;
}

/* CONTENT */
section{
    padding:40px;
    text-align:center;
}

button{
    background:#27ae60;
    color:white;
    padding:14px 22px;
    border:none;
    font-size:17px;
    border-radius:6px;
    cursor:pointer;
}

/* CARD */
.complex-card{
    width:320px;
    margin:40px auto;
}

.complex-photo{
    width:100%;
    border-radius:12px;
    box-shadow:0 4px 12px rgba(0,0,0,0.3);
}

.complex-btn{
    margin-top:15px;
    padding:18px;
    font-size:18px;
    border-radius:12px;
}

/* ===== MOBILE ===== */
@media(max-width:768px){

.menu{
    display:none;
    flex-direction:column;
    position:absolute;
    right:10px;
    top:60px;
    background:#d6a65c;
    padding:15px;
    border-radius:8px;
}

.menu.show{
    display:flex;
}

.menu-icon{
    display:block;
}

.site-title{
    font-size:20px;
}

.logo{
    height:38px;
}

}

</style>

<script>
function toggleMenu(){
    document.getElementById("menu").classList.toggle("show");
}
</script>

</head>

<body>

<!-- NAVBAR -->
<div class="navbar">

<img src="AVS1.png" class="logo">

<h1 class="site-title">Ahobilam</h1>

<div style="display:flex;align-items:center;gap:15px;">

<div class="menu" id="menu">
<a href="#about">About</a>
<a href="#hotels">Hotels</a>
<a href="#temple">Temple</a>
</div>

<div class="menu-icon" onclick="toggleMenu()">☰</div>

<img src="without_bg.png" class="logo">

</div>

</div>

<!-- HEADER -->
<header>
<h1>Ahobilam Rooms</h1>
<p>
<strong>Welcome to Ahobilam Rooms</strong><br>
Your ideal accommodation near the sacred Ahobilam Temple.
</p>
</header>

<!-- FACILITIES -->
<section id="about">

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

<!-- HOTEL -->
<section id="hotels">

<div class="complex-card">

<img src="Rajeshwari.Complex.jpeg" class="complex-photo">

<button class="complex-btn"
onclick="location.href='rooms.html'">
Rajeshwari Complex<br>Book Now
</button>

</div>

</section>

</body>
</html>

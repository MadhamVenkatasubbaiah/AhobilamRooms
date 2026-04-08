<!DOCTYPE html>
<html>
<head>
<title>Ahobilam Rooms</title>

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>

/* ===== BODY ===== */
body{
    font-family: Arial;
    margin:0;
    background:#FFF8E1;
}

/* ===== NAVBAR ===== */
.navbar{
    display:flex;
    align-items:center;
    justify-content:space-between;
    background:#d6a65c;
    padding:10px 20px;
    position:fixed;
    top:0;
    width:100%;
    z-index:1000;
    box-sizing:border-box;
}

.nav-left,
.nav-right{
    display:flex;
    align-items:center;
    gap:15px;
}

.logo{
    height:60px;
    width:auto;
}

/* TITLE CENTER */
.site-title{
    color:white;
    margin:0;
    font-size:32px;
    text-align:center;
    flex:1;
}

/* MENU */
.menu{
    display:flex;
    gap:20px;
}

.menu a{
    color:white;
    text-decoration:none;
    font-weight:bold;
}

/* MOBILE ICON */
.menu-icon{
    display:none;
    font-size:28px;
    color:white;
    cursor:pointer;
}

/* ===== HEADER SECTION ===== */
header{
    margin-top:100px;
    background:#e6b56b;
    color:white;
    padding:80px 20px;
    text-align:center;
    position:relative;
    overflow:hidden;
}

/* WATERMARK IMAGE */
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
    opacity:0.15;
}

/* HEADER TEXT ABOVE WATERMARK */
header *{
    position:relative;
    z-index:2;
}

/* ===== CONTENT ===== */
section{
    padding:40px;
    text-align:center;
}

button{
    background:#27ae60;
    color:white;
    padding:15px 25px;
    border:none;
    font-size:18px;
    cursor:pointer;
    border-radius:5px;
}

/* ===== COMPLEX CARD ===== */
.complex-card{
    width:320px;
    margin:40px auto;
    text-align:center;
}

.complex-photo{
    width:300px;
    border-radius:12px;
    display:block;
    margin:auto;
    box-shadow:0 4px 12px rgba(0,0,0,0.3);
}

.complex-btn{
    background:#27ae60;
    color:white;
    padding:20px;
    border:none;
    font-size:20px;
    border-radius:15px;
    cursor:pointer;
    margin-top:15px;
}

/* ===== MOBILE RESPONSIVE ===== */
@media(max-width:768px){

.menu{
    display:none;
    flex-direction:column;
    position:absolute;
    right:20px;
    top:70px;
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
    font-size:22px;
}

.logo{
    height:45px;
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

<!-- ===== NAVBAR ===== -->
<div class="navbar">

    <div class="nav-left">
        <img src="AVS1.png" class="logo">
    </div>

    <h1 class="site-title">Ahobilam</h1>

    <div class="nav-right">

        <div class="menu" id="menu">
            <a href="#about">About</a>
            <a href="#hotels">Hotels</a>
            <a href="#temple">Temple Timings</a>
        </div>

        <div class="menu-icon" onclick="toggleMenu()">☰</div>

        <img src="without_bg.png" class="logo">

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

<!-- ===== FACILITIES ===== -->
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

<!-- ===== HOTEL CARD ===== -->
<section id="hotels">

<div class="complex-card">

<img src="Rajeshwari.Complex.jpeg" class="complex-photo">

<button class="complex-btn"
onclick="location.href='rooms.html'">
Rajeshwari Complex<br>
Book Now
</button>

</div>

</section>

</body>
</html>

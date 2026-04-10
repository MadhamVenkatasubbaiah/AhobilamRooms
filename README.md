<!-- <!DOCTYPE html> -->
<html>
<head>

<!--<
meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ahobilam Rooms</title>
-->

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
    background:#FFF8E1;
    height:100px;
    padding:0 12px;
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    box-sizing:border-box;
}

/* LOGOS */
.logo{
    height:70px;
    width:auto;
}

/* TITLE */
.site-title{
    color:white;
    margin:0;
    font-size:30px;
    text-align:center;
    flex:1;
}

/* MENU */
.menu{
    display:flex;
}

.menu a{
    text-decoration:none;
    color:white;
    font-weight:bold;
    font-size:20px;
    margin-left:20px;
}

/* MOBILE MENU BUTTON */
.menu-toggle{
    display:none;
    font-size:24px;
    color:white;
    cursor:pointer;
}

/* ===== MOBILE VIEW ===== */
@media(max-width:768px){

.menu{
    display:none;
    flex-direction:column;
    position:absolute;
    top:55px;
    right:0;
    background:#d6a65c;
    width:100%;
    text-align:center;
}

.menu a{
    padding:12px;
    border-top:1px solid rgba(255,255,255,0.3);
}

.menu.show{
    display:flex;
}

.menu-toggle{
    display:block;
}

.site-title{
    font-size:18px;
}
}

/* ===== HEADER WITH WATERMARK ===== */
header{
    margin-top:55px;
    padding:90px 20px;
    text-align:center;
    color:white;
    position:relative;
    background:#e8b97a;
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
    opacity:0.08; /* watermark effect */
}

/* HEADER TEXT ABOVE WATERMARK */
header h1,
header p{
    position:relative;
    z-index:2;
}

/* ===== SECTION ===== */
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

/* COMPLEX CARD */
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

</style>
</head>

<body>

<!-- ===== NAVBAR ===== -->
<div class="navbar">

    <img src="AVS3.png" class="logo">

    <h1 class="site-title">Ahobilam123</h1>

    <img src="without_bg.png" class="logo">

    <div class="menu-toggle" onclick="toggleMenu()">☰</div>

    <div class="menu" id="menu">
        <a href="#">About</a>
        <a href="#">Hotels</a>
        <a href="#">Temple Timings</a>
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

<!-- ===== ROOM CARD ===== -->
<div class="complex-card">

<img src="Rajeshwari.Complex.jpeg" class="complex-photo">

<button class="complex-btn"
onclick="location.href='rooms.html'">
Rajeshwari Complex<br>
Book Now
</button>

</div>

<!-- ===== MOBILE MENU SCRIPT ===== -->
<script>
function toggleMenu(){
    document.getElementById("menu").classList.toggle("show");
}
</script>

</body>
</html>

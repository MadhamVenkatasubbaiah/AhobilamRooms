<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ahobilam Rooms</title>

<style>

/* ---------- BODY ---------- */
body{
    margin:0;
    font-family:Arial;
    background:#FFF8E1;
}

/* ---------- NAVBAR ---------- */
.navbar{
    display:flex;
    align-items:center;
    justify-content:space-between;
    background:#d6a65c;
    padding:8px 20px;
    position:fixed;
    top:0;
    width:100%;
    z-index:1000;
}

/* logo sizes */
.logo-left,
.logo-right{
    height:65px;
    width:auto;
}

/* title center */
.site-title{
    color:white;
    margin:0;
    font-size:32px;
    text-align:center;
    flex:1;
}

/* menu */
.menu{
    display:flex;
    gap:20px;
}

.menu a{
    color:white;
    text-decoration:none;
    font-weight:bold;
}

/* ---------- MOBILE MENU ---------- */
.menu-icon{
    display:none;
    font-size:28px;
    color:white;
    cursor:pointer;
}

/* ---------- HEADER WATERMARK ---------- */
header{
    margin-top:90px; /* fix navbar overlap */
    padding:120px 20px;
    text-align:center;
    color:white;

    /* WATERMARK IMAGE */
    background:
        linear-gradient(rgba(230,180,110,0.9),
        rgba(230,180,110,0.9)),
        url("without_bg.png");

    background-size:300px;
    background-repeat:no-repeat;
    background-position:center;
    background-attachment:fixed;
}

header h1{
    font-size:40px;
}

/* ---------- SECTION ---------- */
section{
    text-align:center;
    padding:40px;
}

button{
    background:#27ae60;
    color:white;
    padding:15px 25px;
    border:none;
    font-size:18px;
    border-radius:6px;
    cursor:pointer;
}

/* ---------- ROOM CARD ---------- */
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
    padding:20px;
    border:none;
    font-size:22px;
    border-radius:15px;
    cursor:pointer;
}

/* ---------- MOBILE RESPONSIVE ---------- */
@media(max-width:768px){

.menu{
    display:none;
    flex-direction:column;
    background:#d6a65c;
    position:absolute;
    top:70px;
    right:0;
    width:200px;
    padding:15px;
}

.menu.show{
    display:flex;
}

.menu-icon{
    display:block;
}

.site-title{
    font-size:24px;
}

.logo-left,
.logo-right{
    height:50px;
}

header{
    padding:80px 15px;
}

}

</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">

    <img src="AVS1.png" class="logo-left">

    <h1 class="site-title">Ahobilam</h1>

    <div class="menu" id="menu">
        <a href="#about">About</a>
        <a href="#hotels">Hotels</a>
        <a href="#temple">Temple</a>
    </div>

    <div class="menu-icon" onclick="toggleMenu()">☰</div>

    <img src="without_bg.png" class="logo-right">

</div>

<!-- HEADER WITH WATERMARK -->
<header>
<h1>Ahobilam Rooms</h1>
<p>
Welcome to Ahobilam Rooms<br>
Your ideal accommodation near the sacred Ahobilam Temple.
</p>
</header>

<!-- CONTENT -->
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

<!-- ROOM CARD -->
<div class="complex-card">

<img src="Rajeshwari.Complex.jpeg" class="complex-photo">

<button class="complex-btn"
onclick="location.href='rooms.html'">
Rajeshwari Complex<br>
Book Now
</button>

</div>

<!-- MOBILE MENU SCRIPT -->
<script>
function toggleMenu(){
    document.getElementById("menu").classList.toggle("show");
}
</script>

</body>
</html>

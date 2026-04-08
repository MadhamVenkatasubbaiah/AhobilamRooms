<!DOCTYPE html>
<html>
<head>
<title>Ahobilam Rooms</title>

<style>
body{
    font-family: Arial;
    margin:0;
    background:#FFF8E1;
}

/* NAVBAR */
.navbar{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:10px 20px;
    background:#d6a65c;

    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
}

/* TRANSPARENT LOGO */
.logo{
    height:100px;
    width:100px;
    object-fit:contain;
    background:transparent;
    display:block;
}

.site-title{
    margin:0;
    color:white;
}

.menu a{
    margin-left:20px;
    text-decoration:none;
    color:white;
    font-weight:bold;
}

/* iframe background area */
.logo-frame{
    margin-top:120px;
    width:100%;
    height:120px;
    border:none;
    background:transparent;
}

/* CONTENT */
header{
    background:#FFCC80;
    color:white;
    padding:80px;
    text-align:center;
}

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

.complex-card{
    width:320px;
    margin:40px;
    text-align:left;
}

.complex-photo{
    width:300px;
    border-radius:12px;
    display:block;
    margin:0 auto 15px auto;
    box-shadow:0 4px 12px rgba(0,0,0,0.3);
}

.complex-btn{
    background:#27ae60;
    color:white;
    padding:30px;
    border:none;
    font-size:25px;
    border-radius:20px;
    cursor:pointer;
}
</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">

    <img src="AVS1.png" class="logo">
    <h1 class="site-title">Ahobilam</h1>
    <img src="without_bg.png" class="logo">

    <div class="menu">
        <a href="#about">About</a>
        <a href="#hotels">Hotels</a>
        <a href="#temple">Temple Timings</a>
    </div>

</div>

<!-- BACKGROUND FROM logo.html -->
<iframe src="logo.html" class="logo-frame" scrolling="no"></iframe>

<header>
<h1>Ahobilam Rooms</h1>
<p><strong>Welcome to Ahobilam Rooms</strong><br>
your ideal accommodation near the sacred Ahobilam Temple.
</p>
</header>

<section>
<h2>Welcome</h2>

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

<div class="complex-card">

<img src="Rajeshwari.Complex.jpeg" class="complex-photo">

<button class="complex-btn"
onclick="location.href='rooms.html'">
Rajeshwari Complex<br>
Book Now
</button>

</div>

</body>
</html>

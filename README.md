<html>
<head>

<div class="navbar">
    <!-- Title -->
    <h1 class="site-title"> Ahobilam </h1>
    <!-- Title -->
    <img src="without_bg" class="logo" alt="Ahobilam Temple Logo">
    <!-- Menu -->
    <div class="menu">
        <a href="#about">About</a>
        <a href="#hotels">Hotels</a>
        <a href="#temple">Temple Timings</a>
    </div>
</div>


<head>
<title>Ahobilam Rooms</title>

</head>
<iframe src="logo.html" 
        style="border:20px;height:100px;width:100%;">
</iframe>

<style>
body{
font-family: Arial;
margin:0;
background:#FFF8E1;
}

/* ✅ ADD NAVBAR CSS HERE */
.navbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:10px 20px;
    background:#d6a65c;

    position:fixed;   /* sticky */
    top:0;
    left:0;
    width:100%;
    z-index:1000;
}

.menu a{
    margin-left:20px;
    text-decoration:none;
    color:white;
    font-weight:bold;
}

.site-title{
    margin:0;
    color:white;
}
.logo{
    height:100px;     /* navbar height ki match */
    width:100px;      /* image stretch avvakunda */
}

<!-- Don'ttouch below lines -->
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
margin:40px 0 40px 40px; /* move to left */
text-align:left;
}

/* image */
.complex-photo{
width:300px;
height:auto;
border-radius:12px;
display:block;
margin:0 auto 15px auto;
box-shadow:0 4px 12px rgba(0,0,0,0.3);
}

/* button */
.complex-btn{
background:#27ae60;
color:white;
padding:30px 30px;
border:none;
font-size:25px;
border-radius:20px;
cursor:pointer;
}  
    
</style>
</head>

<body>

<header>
<h1>Ahobilam Rooms</h1>
<p><strong> Welcome to Ahobilam Rooms </strong><br>
    your ideal accommodation
    near the sacred Ahobilam Temple. We provide clean, comfortable,
    and affordable rooms with a peaceful atmosphere, perfect for
    pilgrims and families seeking a pleasant stay.
</p>
</header>

<section>
<h2>Welcome</h2>
<p>Clean rooms available for pilgrims and families visiting Ahobilam.</p>


    
<h3>Facilities</h3>
<p>✅ AC & Non-AC Rooms<br>
✅ Hot Water 24 Hours <br>
✅ Parking Available<br>
✅ Family Friendly</p>

<button onclick="location.href='tel:+917675962840'">
Call For Booking
</button>
</section>


<div class="complex-card">

    <img src="Rajeshwari.Complex.jpeg"
    alt="Rajeshwari Complex"
    class="complex-photo">
    <button onclick="location.href='rooms.html'">
            Rajeshwari Complex <br>
               Book Now
    </button>

</div>
<!--
<nav>
    <a href="rooms.html"></a>
</nav>
-->

</body>
</html>

<html>
<head>
<style>

/* ===== BODY ===== */
body{
    margin:0;
    font-family:Arial;
    background:#111;
    color:white;
}

/* ===== NAVBAR ===== */
.navbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:15px 40px;
    background:black;
    position:fixed;
    width:100%;
    top:0;
    z-index:1000;
}

/* LEFT LOGO */
.logo{
    display:flex;
    align-items:center;
    gap:10px;
    color:#d4af37;
}

.logo img{
    height:40px;
}

.logo h2{
    margin:0;
    font-size:20px;
}

/* MENU */
.menu{
    display:flex;
    gap:30px;
    align-items:center;
}

.menu a{
    color:#ccc;
    text-decoration:none;
    font-size:16px;
}

.menu a:hover{
    color:#d4af37;
}

/* BOOK BUTTON */
.book-btn{
    background:#d4af37;
    color:black;
    padding:10px 20px;
    border-radius:6px;
    font-weight:bold;
}

/* ===== HERO SECTION ===== */
.hero{
    height:100vh;
    background:url("Rajeshwari.Complex.jpeg") no-repeat center;
    background-size:cover;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    position:relative;
}

/* DARK OVERLAY */
.hero::before{
    content:"";
    position:absolute;
    width:100%;
    height:100%;
    background:rgba(0,0,0,0.6);
}

/* HERO CONTENT */
.hero-content{
    position:relative;
    z-index:2;
}

.hero h1{
    font-size:60px;
    color:#d4af37;
    margin:0;
}

.hero p{
    font-size:20px;
    color:#ccc;
}

/* BUTTONS */
.hero-buttons{
    margin-top:20px;
}

.hero-buttons button{
    padding:12px 25px;
    margin:10px;
    border:none;
    cursor:pointer;
    border-radius:5px;
}

.whatsapp-btn{
    background:#d4af37;
    color:black;
    font-weight:bold;
}

.view-btn{
    background:transparent;
    border:1px solid #d4af37;
    color:#d4af37;
}

/* ===== RESPONSIVE ===== */
@media(max-width:768px){
    .menu{
        display:none;
    }

    .hero h1{
        font-size:35px;
    }
}

</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">

<div class="logo">
<img src="logo.png">
<h2>Madam Rajeswari<br><small>COMPLEX</small></h2>
</div>

<div class="menu">
<a href="#">Home</a>
<a href="#">Rooms</a>
<a href="#">Temple History</a>
<a href="#">Contact</a>
<a href="tel:+917675962840" class="book-btn">📞 Book Now</a>
</div>

</div>

<!-- HERO SECTION -->
<div class="hero">

<div class="hero-content">

<p>WELCOME TO</p>

<h1>Madam Rajeswari<br>Complex</h1>

<p>Ahobilam, Andhra Pradesh</p>
<p>Your divine stay near the sacred Narasimha temples</p>

<div class="hero-buttons">
<button class="whatsapp-btn" onclick="window.location.href='https://wa.me/917675962840'">
Book via WhatsApp
</button>

<button class="view-btn">
View Rooms
</button>
</div>

</div>

</div>

</body>
</html>

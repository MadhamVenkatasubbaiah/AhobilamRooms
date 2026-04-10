<!-- <!DOCTYPE html> -->
<html>
<head>

<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ahobilam Rooms</title>

<style>

/* ===== BODY ===== */
body{
    font-family: Arial;
    margin:0;
    background:#FFF8E1;
}

/* ===== NAVBAR ===== */
.navbar {
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: center;

    background: #FF9933;
    height: 100px;
    padding: 0 20px;

    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;

    box-sizing: border-box;
}

.center {
    text-align: center;
}

.center h1 {
    margin: 0;
    color: white;
    font-size: 32px;
}

/* MENU */
.menu {
    display: flex;
    justify-content: center;
    gap: 30px;
    margin-top: 5px;
}

.menu a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

/* RIGHT */
.right{
    display:flex;
    align-items:center;
    gap:10px;
}

/* HAMBURGER */
.menu-toggle{
    display:none;
    font-size:28px;
    color:white;
    cursor:pointer;
}

/* MOBILE */
@media(max-width:768px){

.menu{
    display:none;
    flex-direction:column;
    position:fixed;
    top:100px;
    left:0;
    background:#d6a65c;
    width:100%;
    text-align:center;
}

.menu a{
    padding:15px;
    border-top:1px solid rgba(255,255,255,0.3);
}

.menu.show{
    display:flex;
}

.menu-toggle{
    display:block;
}

/* hide AVS */
.right img{
    display:none;
}

.center h1{
    font-size:24px;
}
}

/* ===== HEADER ===== */
header{
    margin-top:100px;
    padding:80px 20px;
    text-align:center;
    background:#e8b97a;
    color:white;
}

/* ===== SECTION ===== */
section{
    padding:40px;
    text-align:center;
}

/* BUTTONS */
.btn{
    background:#27ae60;
    color:white;
    padding:12px 20px;
    border:none;
    font-size:16px;
    margin:10px;
    border-radius:6px;
    cursor:pointer;
}

/* BOX */
.box{
    background:white;
    padding:20px;
    margin:20px auto;
    max-width:400px;
    border-radius:10px;
    box-shadow:0 3px 10px rgba(0,0,0,0.2);
}

</style>
</head>

<body>

<!-- NAVBAR -->
<div class="navbar">

  <div class="left">
    <img src="logo.png" height="70">
  </div>
  
  <div class="center">
    <h1>AHOBILAM</h1>
    <div class="menu" id="menu">
      <a href="#about">About</a>
      <a href="#details">Basic Details</a>
      <a href="#timings">Temple Timings</a>
    </div>
  </div>
  
  <div class="right">
    <span class="menu-toggle" onclick="toggleMenu()">☰</span>
    <img src="AVS3.png" height="70">
  </div>

</div>

<!-- HEADER -->
<header id="about">
<h1>Ahobilam Rooms</h1>
<p>Your ideal accommodation near the sacred Ahobilam Temple.</p>

<button class="btn" onclick="scrollToSection('details')">Basic Details</button>
<button class="btn" onclick="scrollToSection('timings')">Temple Timings</button>
</header>

<!-- BASIC DETAILS -->
<section id="details">
<h2>Basic Details</h2>

<div class="box">
<p><strong>Location:</strong> Near Ahobilam Temple</p>
<p><strong>Contact:</strong> +91 7675962840</p>
<p><strong>Room Types:</strong> AC / Non-AC</p>
<p><strong>Facilities:</strong> Parking, Hot Water, Family Rooms</p>
</div>

</section>

<!-- TEMPLE TIMINGS -->
<section id="timings">
<h2>Temple Timings</h2>

<div class="box">
<p><strong>Morning:</strong> 6:00 AM – 12:30 PM</p>
<p><strong>Evening:</strong> 3:00 PM – 8:00 PM</p>
<p><strong>Special Days:</strong> Extended Hours</p>
<p><strong>Note:</strong> Timings may vary on festivals</p>
</div>

</section>

<!-- SCRIPT -->
<script>
function toggleMenu(){
    document.getElementById("menu").classList.toggle("show");
}

function scrollToSection(id){
    document.getElementById(id).scrollIntoView({behavior:"smooth"});
}
</script>

</body>
</html>

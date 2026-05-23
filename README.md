<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>M&P Medical Consultancy</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

<style>

body {
  margin:0;
  font-family:'Poppins', sans-serif;
  background:#f5f7fb;
}

/* NAVBAR */
nav {
  position:sticky;
  top:0;
  background:#0a2a66;
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:12px 40px;
  color:white;
}

.logo {
  display:flex;
  align-items:center;
}

.logo img {
  width:55px;
  margin-right:10px;
}

/* HERO */
.hero {
  height:100vh;
  background:linear-gradient(rgba(10,42,102,0.8),rgba(10,42,102,0.8)),
  url('https://images.unsplash.com/photo-1588776814546-ec7e1c0baf55');
  background-size:cover;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  color:white;
  text-align:center;
}

.hero h1 {
  font-size:55px;
}

/* BUTTON */
.btn {
  background:gold;
  padding:12px 25px;
  border:none;
  border-radius:5px;
  font-weight:bold;
  cursor:pointer;
}

/* SECTION */
.section {
  padding:70px 20px;
  text-align:center;
}

/* CARDS */
.cards {
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
}

.card {
  width:260px;
  background:white;
  margin:15px;
  padding:20px;
  border-radius:12px;
  box-shadow:0 10px 25px rgba(0,0,0,0.1);
  transition:0.3s;
}

.card:hover {
  transform:translateY(-10px);
}

/* IMAGE SECTION */
.image-section {
  display:flex;
  flex-wrap:wrap;
}

.image-box {
  width:50%;
  height:300px;
  background-size:cover;
  background-position:center;
}

/* QUOTE */
.quote {
  background:#0a2a66;
  color:white;
  padding:50px;
  font-size:22px;
  font-style:italic;
}

/* FORM */
form {
  max-width:420px;
  margin:auto;
  background:white;
  padding:25px;
  border-radius:10px;
}

input, select {
  width:100%;
  padding:12px;
  margin:10px 0;
}

/* FOOTER */
footer {
  background:#0a2a66;
  color:white;
  padding:20px;
  text-align:center;
}

/* WHATSAPP */
.whatsapp {
  position:fixed;
  bottom:20px;
  right:20px;
  background:#25D366;
  padding:15px;
  border-radius:50%;
  color:white;
  font-size:22px;
  text-decoration:none;
}

</style>

</head>

<body>

<!-- NAVBAR -->
<nav>
  <div class="logo">
    <img src="logo.png">
    <h2>M&P Consultancy</h2>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <h1>Shape Your Medical Career Abroad</h1>
  <p>Study MBBS in Russia & Kyrgyzstan</p>
  <button class="btn" onclick="scrollToForm()">Apply Now</button>
</section>

<!-- IMAGE SECTION -->
<div class="image-section">
  <div class="image-box" style="background-image:url('https://images.unsplash.com/photo-1576765608535-5f04d1e3f289')"></div>
  <div class="image-box" style="background-image:url('https://images.unsplash.com/photo-1580281657527-47e4b6d3e5c9')"></div>
</div>

<!-- QUOTE -->
<div class="quote">
  "The art of medicine consists of amusing the patient while nature cures the disease."
</div>

<!-- COUNTRIES -->
<section class="section">
  <h2>Our Destinations</h2>
  <div class="cards">
    <div class="card">Russia</div>
    <div class="card">Kyrgyzstan</div>
  </div>
</section>

<!-- UNIVERSITIES -->
<section class="section">
  <h2>Top Universities</h2>
  <div class="cards">
    <div class="card">Osh International Medical University</div>
    <div class="card">Osh State University</div>
    <div class="card">Jalal-Abad International University</div>
  </div>
</section>

<!-- SERVICES -->
<section class="section">
  <h2>Our Services</h2>
  <div class="cards">
    <div class="card">Admission Support</div>
    <div class="card">Visa Guidance</div>
    <div class="card">Accommodation</div>
    <div class="card">Travel Assistance</div>
  </div>
</section>

<!-- APPLY FORM -->
<section class="section" id="apply">
  <h2>Apply Now</h2>
  <form onsubmit="sendToWhatsApp(event)">
    <input type="text" id="name" placeholder="Full Name" required>
    <input type="tel" id="phone" placeholder="Phone Number" required>

    <select id="country" required>
      <option value="">Select Country</option>
      <option>Russia</option>
      <option>Kyrgyzstan</option>
    </select>

    <button class="btn">Submit</button>
  </form>
</section>

<!-- FOOTER -->
<footer>
  <p>© 2026 M&P Medical Consultancy</p>
</footer>

<!-- WHATSAPP -->
<a class="whatsapp" href="https://wa.me/918550959998">💬</a>

<script>
function scrollToForm(){
  document.getElementById("apply").scrollIntoView({behavior:'smooth'});
}

function sendToWhatsApp(e){
  e.preventDefault();
  let name=document.getElementById("name").value;
  let phone=document.getElementById("phone").value;
  let country=document.getElementById("country").value;

  let msg=`New Lead:%0AName:${name}%0APhone:${phone}%0ACountry:${country}`;
  window.open(`https://wa.me/918550959998?text=${msg}`);
}
</script>

</body>
</html>

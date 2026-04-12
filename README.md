<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Aurexis Labs — AI Product Studio</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

<link rel="icon" href="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg">

<style>
:root{
--bg:#05070a;
--card:#0f1318;
--text:#f5f7fa;
--muted:#8b949e;
--border:#1f2630;
--accent:#5b7cff;
--glow:#5b7cff55;
}

*{margin:0;padding:0;box-sizing:border-box;font-family:'Inter',sans-serif;}

body{
background:radial-gradient(circle at 20% 20%, #111827, #05070a);
color:var(--text);
scroll-behavior:smooth;
}

/* NAV */
nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:18px 50px;
background:rgba(5,7,10,0.7);
backdrop-filter:blur(10px);
border-bottom:1px solid var(--border);
position:sticky;
top:0;
z-index:1000;
}

.logo{
display:flex;
align-items:center;
gap:10px;
font-weight:600;
}

.logo img{
height:34px;
border-radius:10px;
}

.nav-links a{
margin-left:30px;
text-decoration:none;
color:var(--muted);
font-size:14px;
}

.nav-links a:hover{color:white}

/* HERO */
.hero{
text-align:center;
margin:120px auto;
max-width:900px;
}

.hero-logo{
height:80px;
border-radius:16px;
margin-bottom:20px;
box-shadow:0 0 40px var(--glow);
}

.hero h1{
font-size:56px;
line-height:1.1;
letter-spacing:-1px;
}

.hero p{
margin-top:20px;
color:var(--muted);
font-size:18px;
}

/* BUTTON */
.btn{
display:inline-block;
margin-top:30px;
padding:14px 30px;
border-radius:10px;
background:var(--accent);
color:white;
text-decoration:none;
transition:0.3s;
}

.btn:hover{
transform:translateY(-3px);
box-shadow:0 10px 30px var(--glow);
}

/* SECTION */
section{
max-width:1000px;
margin:100px auto;
padding:0 20px;
opacity:0;
transform:translateY(40px);
transition:0.6s;
}

section.show{
opacity:1;
transform:translateY(0);
}

h2{
font-size:32px;
margin-bottom:10px;
}

.sub{
color:var(--muted);
margin-bottom:30px;
}

/* GRID */
.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
gap:20px;
}

/* CARD */
.card{
background:var(--card);
border:1px solid var(--border);
border-radius:14px;
padding:30px;
transition:0.3s;
}

.card:hover{
transform:translateY(-6px);
box-shadow:0 10px 40px #000;
}

/* CTA */
.cta{
padding:60px;
border-radius:16px;
background:linear-gradient(135deg,#5b7cff,#3a5bff);
text-align:center;
}

/* GLASS CONTACT */
.glass{
background:rgba(255,255,255,0.05);
border:1px solid rgba(255,255,255,0.1);
backdrop-filter:blur(14px);
border-radius:16px;
padding:30px;
box-shadow:0 10px 40px #000;
}

/* FORM */
.contact input,.contact textarea{
width:100%;
padding:14px;
margin-top:12px;
border-radius:8px;
border:1px solid var(--border);
background:#0b0f14;
color:white;
}

/* FOOTER */
footer{
text-align:center;
padding:50px;
color:var(--muted);
border-top:1px solid var(--border);
margin-top:80px;
}
</style>
</head>

<body>

<nav>
<div class="logo">
<img src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg">
<span>Aurexis Labs</span>
</div>

<div class="nav-links">
<a href="#home">Home</a>
<a href="#about">About</a>
<a href="#pricing">Pricing</a>
<a href="#hire">Hire</a>
<a href="#team">Join Team</a>
<a href="#contact">Contact</a>
</div>
</nav>

<!-- HERO -->
<div class="hero" id="home">

<img class="hero-logo" src="https://i.postimg.cc/ZnvffBCg/1dcdb7f7-de7b-48ae-920e-9869e990031b-7C361840-19A8-47AC-B944-81763F2E43D9.jpg">

<h1>Build AI & Software That Wins</h1>
<p>We design and engineer high-performance digital systems.</p>

<a href="#contact" class="btn">Start Project</a>

</div>

<!-- ABOUT -->
<section id="about">
<h2>About</h2>
<p class="sub">Focused on real impact.</p>
<div class="card">
Aurexis Labs builds scalable AI systems, games, and software for modern businesses.
</div>
</section>

<!-- SERVICES -->
<section>
<h2>Services</h2>
<div class="grid">
<div class="card">AI Systems</div>
<div class="card">Game Development</div>
<div class="card">Software Engineering</div>
</div>
</section>

<!-- PRICING -->
<section id="pricing">
<h2>Pricing</h2>
<div class="grid">
<div class="card">Starter — ₹10,000+</div>
<div class="card">Professional — ₹50,000+</div>
<div class="card">Enterprise — Custom</div>
</div>
</section>

<!-- HIRE -->
<section id="hire">
<div class="cta">
<h2>Hire Us For Your Next Project</h2>
<a href="#contact" class="btn">Get Started</a>
</div>
</section>

<!-- TEAM -->
<section id="team">
<h2>Join Team</h2>
<div class="card">
We’re looking for passionate developers and creators.
</div>
</section>

<!-- CONTACT -->
<section id="contact">
<h2>Contact</h2>

<div class="glass">

<form class="contact" action="https://formspree.io/f/xjgepqwn" method="POST">
<input name="name" placeholder="Name" required>
<input name="email" placeholder="Email" required>
<textarea name="message" placeholder="Your idea" required></textarea>
<button class="btn">Send Message</button>
</form>

<p style="margin-top:20px;">
📱 <a href="tel:+917415072867" style="color:white;">+91 7415072867</a><br>
📸 <a href="https://instagram.com/aurexislabs" style="color:white;">@aurexislabs</a>
</p>

</div>

</section>

<footer>
© 2026 Aurexis Labs
</footer>

<script>
let sections=document.querySelectorAll("section");
window.addEventListener("scroll",()=>{
sections.forEach(sec=>{
if(sec.getBoundingClientRect().top < window.innerHeight-100){
sec.classList.add("show");
}
});
});
</script>

</body>
</html>
